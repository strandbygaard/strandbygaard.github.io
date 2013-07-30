---
author: strandbygaard
comments: true
date: 2011-06-10 04:00:31+00:00
layout: post
slug: oc4j-mtom-and-the-huge-problem-of-return-types
title: OC4J, MTOM, and the huge problem of [limited] return types
wordpress_id: 149
categories:
- Development
tags:
- java
---

This one really surprised me.

Webservices implemented on the OC4J stack cannot return types under the java.* namespace, at least up to and including the current version 10.1.3.5. 

This really limits the usefulness of MTOM (Message Transmission Optimization Mechanism) support in OC4J. If you need to deploy webservices on OC4J that return large amounts of data, most likely with MTOM transport enabled, your options appear to be either: don't or use JAX-WS RI.

Try to compile and deploy a webservice with a method signature like:

``` java
public InputStream getPublicationTable() throws RemoteException;
```
and the oracle:assemble ant task will most kindly tell you that:

`Return type java.io.InputStream Can not have a value type in a package under java.*`

Under most circumstances, changing the method signature to something like

``` java
public byte[] getPublicationTable() throws RemoteException;
```

will get you where you want to be, and if data is already binary you might as well MTOM enable the service at the same time.

The above works just fine for exchanging images, PDF files, and similar data, but MTOM enables other usecases than simply avoiding the base64 encoding overhead when transferring images and other binary data using SOAP.

On a current project I'm working on, I need to expose webservices that return data in quantities that are orders of magnitude larger than available server memory. Upwards 100Gb transferred in a single method invocation. The reasons for this can always be debated, but such are the customer's requirements.

In this context the proposed solution doesn't work. That solution requires a server capable of storing the whole byte-array in memory (it's a store'n forward pattern). The solution to this problem with the first solution is normally to introduce some form of data chunking, but that imposes some unwanted properties on the server and the caller such as state and house keeping (how far are we, and far do we have to go). And more importantly, it defies the purpose of letting the infrastructure handle these complexities in the first place.

If you're stuck on OC4J, somewhere around version 10.1.3.x and less than 11g, the only option available seems to be to hook in another WS stack in OC4J, that does support exposing streams as return types. Luckily, Oracle provides some decent [information](http://download.oracle.com/docs/cd/E12524_01/web.1013/e12290/opensrc.htm#BABDDAIF) on doing so, though you will loose all the nice tooling support available in a pure OC4J stack.

If you're lucky enough to be on [Metro](http://metro.java.net/), [this](http://metro.java.net/guide/Large_Attachments.html) is how you do it. It's also worth reading [this](http://stackoverflow.com/questions/132590/can-a-web-service-return-a-stream) on [Stackoverflow](http://www.stackoverflow.com).
