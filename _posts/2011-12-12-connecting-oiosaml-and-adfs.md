---
author: Martin Strandbygaard
comments: true
date: 2011-12-12 06:00:00+00:00
layout: post
title: Connecting OIOSAML.net And AD FS2.0
categories: Identity
tags: [ADFS2, OIOSAML.net, SAML2]
---

{% include JB/setup %}

In this post, I'll go over the required steps on AD FS2.0 to successfully set up an OIOSAML.net based relying party. The key to success are three specific claim rules, and a single change to the default configuration.

OIOSAML.Net provides a mature framework for creating SAML2.0 based federations between an ASP.Net based relying party, and an identity provider such as Microsoft AD FS2.0, and it only requires minimal configuration on  AD FS2.0 to set up an OIOSAML.net based relying party.

Unfortunately, when the configuration isn't just right, the errors provided by OIOSAML.net can be very arcane and cryptic leading to countless hours spent troubleshooting a seemingly very simple task. The reason being, that the OIOSAML.Net framework performs strict checking of the OIO Web SSO Profile.

##### Claim Rules

Three claim rules are a precondition to federating OIOSAML.net with AD FS2.0:

1. Issue the specification version claim
2. Issue the assurance level claim
3. Correctly set NameID

The first two are easily achieved with two simple custom claim rules:

First, add a rule that always issues a claim with type "dk:gov:saml:attribute:SpecVer" and the value "DK-SAML-2.0":

``` cpp
@RuleName="Issue Specification Version (required by OIO Web SSO Profile)"
=> issue(Type = "dk:gov:saml:attribute:SpecVer", Value = "DK-SAML-2.0"); 
```

Next, add a rule that issues a claim with type "dk:gov:saml:attribute:AssuranceLevel", and a value matching the assurance level of the chosen authentication method:

``` cpp
@RuleName="Issue Assurance Level (required by OIO Web SSO Profile)"
=> issue(Type = "dk:gov:saml:attribute:AssuranceLevel", Value = "3"); 
```
The last requirement, setting the NameID, can be achieved in a number of ways. A quick, initial, approach is to pass through a Name claim:

``` cpp
@RuleName="Pass through Name Claim"
c:[Type == "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name"] => issue(claim = c);
```

And transform it to a persistent NameID:

``` cpp
@RuleName="Map Name Claim To NameID"
@RuleTemplate = "MapClaims"
c:[Type == "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name"] => issue(Type = "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/nameidentifier", Issuer = c.Issuer, OriginalIssuer = c.OriginalIssuer, Value = c.Value, ValueType = c.ValueType, Properties["http://schemas.xmlsoap.org/ws/2005/05/identity/claimproperties/format"] = "urn:oasis:names:tc:SAML:2.0:nameid-format:persistent");
```

##### Changing Signature Algorithm

AD FS2.0 defaults to SHA-256 for signature algorithm, which is supported by the Windows Identity Foundation Framework (WIF), and not much else. If you're federating most anything not based on WIF with AD FS2.0, then you likely need to change the signature algorithm from SHA-256 to SHA-1. This is also the case with OIOSAML.net

This configuration hides under AD FS2.0 > Trust Relationships > Relying Party Trusts > [your RP] > Properties > Advanced

![](/images/2011-12-12-connecting-oiosaml-and-adfs/20111212-104940.png)
