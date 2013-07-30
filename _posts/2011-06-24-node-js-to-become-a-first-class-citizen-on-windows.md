---
author: strandbygaard
comments: true
date: 2011-06-24 08:00:50+00:00
layout: post
slug: node-js-to-become-a-first-class-citizen-on-windows
title: Node.js to become a first class citizen on Windows
wordpress_id: 178
categories:
- Development
tags:
- Node.js
---

This is the best news I've had all week!

[Microsoft](http://blogs.msdn.com/b/interoperability/archive/2011/06/23/microsoft-working-with-joyent-and-the-node-community-to-bring-node-js-to-windows.aspx) and [Joyent](http://joyeur.com/2011/06/23/joyent-partners-with-ms-to-port-node-js-to-windows/) have announced that they will work towards making Windows a supported platform for [Node.js](http://nodejs.org/)

If you live in a Windows shop, it will no longer be political suicide to suggest a Node-solution. Well, at least less :-)

The event driven nature of Node.js, is just a much better solution to many problems, than the more traditional per-request threading model that many web servers employ. Handling 10.000 long running requests on IIS is no fun, but it's a breeze in Node.js

For some nails, Node.js is simply a much better hammer! That it also scales really well, is an added bonus.

At the moment Node.js solutions can really only be deployed on *nix platforms. Node.js does run on Windows, but everything about doing so is a hassle and it's Cygwin cage hampers performance. Unfortunately, most Windows shops are terrified of anything non-conformant, which often means solving problems with 'approved' tools, rather than the best tools, effectively ruling out Node-solutions deployed on anything non-Windows.

This news brought Node.js a little closer to becomming an approved tool, rather than just being the best :-)
