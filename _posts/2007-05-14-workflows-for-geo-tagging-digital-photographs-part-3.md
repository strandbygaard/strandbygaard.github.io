---
author: Martin Strandbygaard
comments: true
date: 2007-05-14 04:00:00+00:00
layout: post
slug: workflows-for-geo-tagging-digital-photographs-part-3
title: Workflows for Geo-Tagging Digital Photographs (part 3)
wordpress_id: 31
categories:
- Photography
tags: [RAW, GPS, Geotagging]
---

### Synchronizing GPS Track Logs And EXIF Data

It doesn’t take a great leap of imagination to see, that combining a GPS track log with the EXIF data in an image, will show the proximity of where that image was taken. On the face of it, bringing along a small GPS unit with your camera sounds like an easy thing to do, so this solution should be close to ideal - and it probably is for many people - but I have to admit that I’ve really taken to this approach. The practicalities of the actual doing always seem to get in my way.

Things do have to line up, to successfully compare two sets with many data points. The GPS unit must have the right time and time zone _before_ you start recording the track log. If you’re moving between locations, the distance may cause the GPS unit to take a few minutes to get a fix, which can be an eternity in photography.

Similarly, the camera has to be configured correctly. Almost all photography oriented image processing software contains a feature to correct (apply an offset to) the EXIF capture date/time, and there’s a reason for this: You (well, at least I) frequently need it. If the camera time is wrong (incorrect clock, daylight savings, time zone), and you don’t notice this until you’ve already taken a number of pictures, the resulting mess of having to split up the pictures in smaller groups corresponding to time settings is a real pain. So far I’ve ended up in this situation every single time I’ve traveled outside GMT+1 where I live, and again when I’ve returned home.

So, I find that something that sounds like an almost perfect solution is far from, but although I’m fairly methodical in the way I work, judging from posts I’ve read on the Internet, this approach does work for many people. That being said, now I’ll cover how I go about doing this (I have put great effort into making this solution work for me).

### Preparing The Camera and GPS Unit 

As I’ve already hinted at, proper pre-configuration makes all the difference. For me I’ve come up with a small checklist I keep wrapped around my GPS unit which will remind me what to do whenever I consider using this method. The procedure I’ve come up with is:

  1. Set timezone on GPS device
  2. Take picture of GPS unit showing current time
  3. Set camera time
  4. Set camera timezone
  5. Set daylight saving
  6. Take picture of GPS unit showing current time

Step two is optional and is used to identity where in the sequence of images I changed the time settings. Step six is redundant if three and four are done correctly, but I do this anyway just to be sure I know the offset, if I made a mistake.

Note: Most smaller Garmin units (eTrex, Legend, Vista, etc.) will only keep time data for _the active track_, so if you save a track to start on a new you loose the ability to match timestamps which is the whole basis of the exercise. I have no idea if other manufacturer’s units do the same, but keep this in my if you’re using a Garmin unit.

### Synchronizing GPS Track Log And Image Files

Once a number of photographs have been taken while simultaneously recording a GPS track log it’s time to combine the two, and provided that everything was configured correctly, that’s quickly handled.

At first I created a shell script based on [exiftool](http://www.sno.phy.queensu.ca/%7Ephil/exiftool/) to do this and later switched to [gpsPhoto.pl](http://www.carto.net/projects/photoTools/gpsPhoto/) which does the same thing (and much more), however it didn’t  
take long for someone to create GUI based applications to do this.

On Mac I believe the defacto standard is the freely available [GPSPhotoLinker](http://oregonstate.edu/%7Eearlyj/gpsphotolinker/), especially after RAW format support was added, but [GeoTagging Automator Action](http://www.scriptamac.at/geotaggingactions.html) can also be used to create a semi-GUI approach. On Windows, [RoboGEO](http://www.robogeo.com/) looks very nice, but I haven’t tested it. 

[![workflows-for-geo-tagging-digital-photographs-part-3.png](http://www.strandbygaard.net/wp-content/uploads/2007/06/workflows-for-geo-tagging-digital-photographs-part-3.png)](http://www.strandbygaard.net/wp-content/uploads/2007/06/workflows-for-geo-tagging-digital-photographs-part-3.png)

### Missing Link(s)

Given the low technical complexity involved in synchronizing EXIF data and GPS track logs, I wondered it isn’t a feature in any of the pro-oriented imaging software tools like [Aperture](http://www.apple.com/aperture/)/[Lightroom](http://www.adobe.com/products/photoshoplightroom/) or [Photo Mechanics](http://www.camerabits.com/)/[Breeze Browser](http://www.breezesys.com/BreezeBrowser/), and other DAM software. Adding yet another application, external to the organizer of choice adds up to a lot of extra work, and this would be a low cost and high visibility feature to implement, but I’ll elaborate on the overlooked possibilities there in another different post.
