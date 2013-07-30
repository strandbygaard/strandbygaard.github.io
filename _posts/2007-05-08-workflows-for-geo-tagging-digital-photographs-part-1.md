---
author: Martin Strandbygaard
comments: false
date: 2007-05-08 13:05:35+00:00
layout: post
slug: workflows-for-geo-tagging-digital-photographs-part-1
title: Workflows for Geo-Tagging Digital Photographs (part 1)
wordpress_id: 10
categories:
- Photography
tags: [RAW, GPS, Geotagging]
---

### Introduction

In this five part blog post I'll describe three different techniques for efficiently geo-tagging digital photographs:

  * Manual batch tagging during post-processing
  * GPS track log synchronization during post-processing
  * In-camera tagging during shooting

The techniques are suitable for high volume shooting, and for different shooting conditions. Although the techniques are independent of the image format, I'll focus on raw image files, and the tools I mention have been chosen accordingly. 

I use a Mac, and all applications are Mac only, though I'm sure similar applications exist for Windows. Although the techniques do to some extent overlap in their application, I've found that all three are necessary to address all shooting conditions.

### Background

The freely available mapping tools that have become available over the last couple of years, with Google Earth and Maps leading the pack, make for some very interesting presentation platforms for photographic material.

Physical image medias such as negatives were limited to one physical sort order (e.g. by date, client, location, etc.), that could be extended with additional indexed sort orders, at a (comparatively) significant additional amount of work. Digital asset management applications (DAM) such as Portfolio, Iview, Aperture/Lightroom, and others or even just the filesystem have already shown their versatility in allowing instant sort orders based on any metadata assigned to the digital asset, e.g. a digital photograph.

![](/images/2007-05-08-workflows-for-geo-tagging-digital-photographs-part-1/picture-1-4-1.jpg)

However, even DAM is limited to only semi-automatic tagging and metadata assignment, still requiring a fair amount of human work to properly classify each image, and for the inexperienced user, the result is often very unstructured.

Unlike old-style location based sorting, e.g. "Yosemite, Half Dome", high precision geographic mapping and presentation of photographs based on shooting location coordinates makes it possible to infer metadata about the photographs, using available map search tools from Google and Yahoo, without any additional human work, by combining search terms and location data in search queries.

Many web services (e.g. [Flickr](http://www.flickr.com/), [Panoramio](http://www.panoramio.com/), [Zooomr](http://www.zooomr.com/)) already offer this type of image content search and new sites that integrate images, maps, and search appear all the time.

Common to all these services is that they require the images to be tagged with the shooting location as EXIF metadata (geo tagging), and while most of these services offer interfaces for manually geo-tagging individual images, this approach is generally too time consuming for any kind of serious image volume, hence a different approach is desirable.

### Geo-Tagging Techniques

There are two fundamental approaches to obtaining the location data of images:

  * Recording the coordinates at shoot-time using e.g. a GPS device	
  * Looking up the coordinates post-shoot

If possible recording the coordinates using a GPS device gives more precise coordinates for each image, but unfortunately this is rarely possible when shooting indoors as most GPS devices don't work indoors. In these situations it is necessary to lookup the approximate coordinates on a map or take a location reading outside the building using a GPS device.

Fortunately, when shooting indoors you normally won't be moving around a very big area, so in this case looking up the coordinates has less impact.

Recording GPS coordinates can be done using either a separate GPS device, connecting a GPS device to the camera, or using a camera with a built in GPS receiver. At this time, Ricoh is the only brand to offer a camera with a built in reciver, and this model is intended for any serious shooting, so the latter option is not really an option, although I suspect we'll very soon start seeing many more camera models with built in GPS receivers.

_In the next part, I'll cover how to manually tag batches of images during post-processing ...._



