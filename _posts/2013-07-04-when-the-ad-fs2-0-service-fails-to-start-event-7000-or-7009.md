---
author: Martin Strandbygaard
comments: true
date: 2013-07-04 11:04:15+00:00
layout: post
slug: when-the-ad-fs2-0-service-fails-to-start-event-7000-or-7009
title: When The AD FS2.0 Service Fails To Start (Event 7000 or 7009)
categories: Identity
tags: [ADFS2]
---

{% include JB/setup %}

There can be many reasons, and the following solution is rarely it, but when the following error does occur in the eventlog:

`A timeout was reached (30000 milliseconds) while waiting for the AD FS 2.0 Windows Service service to connect.`

It can be difficult to troubleshoot, and Google fails to turn up a solution. Usually, the solution is to increase the service start timeout value. Just do this:

[http://support.microsoft.com/kb/922918](http://support.microsoft.com/kb/922918)

On the internal AD FS2.0 server, the problem usually occurs, when it takes more than 30 seconds to connect to the database server, and is mostly seen after the AD FS2.0 server has been restarted.

On an AD FS2.0 proxy, the problem usually occurs because the service takes more than 30 seconds to connect to the internal AD FS2.0 server, and is mostly seen in the last step of the AD FS2.0 proxy configuration wizard.

The error can occur on both internal servers and proxies.