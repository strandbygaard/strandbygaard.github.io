---
author: Martin Strandbygaard
comments: true
date: 2007-06-12 04:00:00+00:00
layout: post
slug: flickr-kml-feed-in-beta
title: Flickr KML Feed In Beta
categories:
- Photography
tags: [Geotagging]
---

If you’re using Flickr, and has [Google Earth](http://earth.google.com/) installed clicking this [link](http://api.flickr.com/services/feeds/geo/?id=74832966@N00&format=kml_nl) says it all. If you don’t have Google Earth, just paste it into [Google Maps](http://maps.google.com/) instead.

With the ability to geotag images ([introduction](http://blog.strandbygaard.net/2007/05/11/workflows-for-geo-tagging-digital-photographs-part-1/), [manually](http://blog.strandbygaard.net/2007/05/11/workflows-for-geo-tagging-digital-photographs-part-2/), [with GPS](http://blog.strandbygaard.net/2007/05/14/workflows-for-geo-tagging-digital-photographs-part-3/), and [in-camera](http://blog.strandbygaard.net/2007/05/17/workflows-for-geo-tagging-digital-photographs-part-4/)) also came the desire to show those images on a map. While EXIF GPS tags have existed for some time, this desire really started to make sense with the advent of applications such as [Google Earth](http://earth.google.com/), [Google Maps](http://maps.google.com/), Yahoo Maps, etc.

Photo sharing sites, such as [Flickr](http://www.flickr.com/), [Zooomr](http://zooomr.com/), and [Panoramio](http://www.panoramio.com/) (now Google) rose to the occasion, but none can IMHO compete with Google Maps and Earth, when it comes to mapping functionality. Both can put images on the maps using KML files, and Google Maps can also show geotagged RSS feeds, and since image feeds from Flickr contains coordinates, it’s just asking for a mashup to convert the feeds from Flickr to a KML file.

[Yahoo Pipes!](http://pipes.yahoo.com/) made that very easy, as I’ve [mentioned](http://www.strandbygaard.net/2007/05/15/creating-a-kml-feed-from-flickr-using-yahoo-pipes/) previously, but the solution was still a bit geeky if IT isn’t your bread and butter, and in many cases even if it is.

Good news. Geobloggers has posted a [lengthy article](http://geobloggers.com/archives/2007/05/31/flickr-kml-and-a-stroll-down-memory-lane/trackback/) about new improvements to geotagged feeds from Flickr. It’s still in beta, but every good web application these days seem to be.

Now Flickr will output KML directly based on parameters such as ID, tags, or groups.

This is an RSS feed of all my geotagged images. Substitute the ID with yours, and you get your own.

[http://api.flickr.com/services/feeds/geo/?id=74832966@N00](http://api.flickr.com/services/feeds/geo/?id=74832966@N00)

Add "&format=kml_nl" and you get a network linked KML file that automatically updates.

[http://api.flickr.com/services/feeds/geo/?id=74832966@N00&format=kml_](http://api.flickr.com/services/feeds/geo/?id=74832966@N00&format=kml_nl)
