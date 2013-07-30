---
author: Martin Strandbygaard
comments: true
date: 2007-06-19 04:00:00+00:00
layout: post
slug: getting-more-interested-in-i-names
title: Getting More Interested In I-Names
wordpress_id: 43
categories:
- Identity
tags: [OpenID]
---

Ever heard of [I-Names](http://i-names.net/)?

I think it holds great promise and have pointed [www.i-names.dk](http://www.openid.dk/www.i-names.dk) to this page, as I’ll be writing more about I-names in the future.

One of my biggest gripes about OpenID is that it requires the user to remember a URL. It’s not intuitive - a URL points to a website, not a person - and OpenID have a tendency to be long and complicated. Even for a native English speaker spelling “myopenid” can be a challenge, not to mention “pip.verisignlabs.com”. True, some will have their “own” URL’s that will resolve to an OpenID which makes things easier, but I would contest that if you can setup this up, URL’s aren’t foreign to you anyway.

Enter [I-Names](http://i-names.net/), a globally unique, human readable, identifier that even has the added advantage of being based on a [number](http://en.wikipedia.org/wiki/I-number) that is transitively unique making it a better identifier.

Instead of being [martin.strandbygaard.myopenid.com](http://martin.strandbygaard.myopenid.com/) I’m suddenly =martin.strandbygaard, and if that’s too long (even the Danish speaking crowd can be challenged spelling my last name), then I can just add another I-name such as =ms that references the same I-number.

Intuitive use of both OpenID and I-Names has a nasty property of encoding unrelated information into the identifier. It may be that only one =martin.strandbygaard is needed, but like e-mail addresses I’m sure we’ll see =john.doe1, =john.doe2, =john.doe3, ….

Architecturally pleasing or not, the Internet user is better off having something like OpenID than not, and with I-names support coming in OpenID v2, there will be someting at least as intuitive as e-mail addresses to be used as identifiers.

(I know, e-mail addresses will also be supported identifiers in OpenID v2 …)
