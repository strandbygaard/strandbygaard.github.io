---
author: strandbygaard
comments: true
date: 2009-09-09 13:07:00+00:00
layout: post
slug: solution-android-browser-displays-blank-page
title: 'Solution: Android Browser Displays Blank Page'
wordpress_id: 58
categories:
- Software
tags:
- Android
---

I've had an HTC Hero for a couple of weeks and save it's at times lackluster speed, I think it's hands down the best handset I've had.

Today, my handset started exhibiting a strange behaviour: Many Google services, e.g. Reader and Tasks would not load, and instead the browser would just show a blank screen. At first it seemed to be related to Google's web sites, but further testing proved it to be all SSL protected web sites that would display the blank screen.

Some Googling turned up many users complaining about this issue (see this [thread](http://code.google.com/p/android/issues/detail?id=3334) on Google Code).

I'm in Denmark and on TDC's network. In my case, the issue was resolved by changing the APN to "internet" and removing the proxy server address and port. Go to Settings -> Wireless Controls -> Mobile Network Settings -> Access Point Names, select the proper configuration (mine was called TDC WAP, but that only holds in DK on TDC's network), and make the relevant changes.

Given the degree in which Mobile operators lock in their users, and the technical difficulty in fixing this, I'm rather disappointed that my network operator doesn't ensure that something as simple as port 443 traffic works on the network.