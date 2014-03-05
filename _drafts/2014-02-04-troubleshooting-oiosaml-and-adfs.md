---
author: Martin Strandbygaard
comments: true
date: 2014-02-04 06:00:00+00:00
layout: post
title: Troubleshooting OIOSAML.net And ADFS
categories: Identity
tags: [ADFS2, ADFS3, OIOSAML.net, SAML2]
---

{% include JB/setup %}

OIOSAML.Net is a great framework for federating ASP.Net web applications using SAML2.0, however sometimes configuration errors on the identity provider can lead to some pretty arcane error messages from OIOSAML.net. This post covers one of those:

![](/images/2014-02-04-troubleshooting-oiosaml-and-adfs/20140204-095100.jpg)
 
The first time you encounter that error it's not readily apparent what the cause is.

Some insight can be found in the test-cases for validating DK-SAML 2.0 profile compliance:

[](https://svn.softwareborsen.dk/oiosaml.net/tags/release-1.7.6/src/dk.nita.saml20/dk.nita.test.saml20/Saml20/DKSAML20ProfileValidationTest.cs)

``` cpp
        /// <summary>
        /// Verify the rules for the &lt;AuthnStatement&gt; element, which are outlined in section 7.1.7 of [DKSAML]
        /// </summary>
        [Test]        
        public void AuthnStatement_Element()
        {
            Assertion saml20Assertion = AssertionUtil.GetBasicAssertion();
            AuthnStatement authnStmt =
                (AuthnStatement)Array.Find(saml20Assertion.Items, delegate(StatementAbstract stmnt) 
                {
                	return stmnt is AuthnStatement; 
                });

            // Mess around with the AuthnStatement.
            {
                string oldSessionIndex = authnStmt.SessionIndex;
                authnStmt.SessionIndex = null;
                TestAssertion(saml20Assertion, "The DK-SAML 2.0 profile requires that the \"AuthnStatement\" element contains the \"SessionIndex\" attribute.");
                authnStmt.SessionIndex = oldSessionIndex;
            }
```
