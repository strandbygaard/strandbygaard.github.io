---
author: Martin Strandbygaard
comments: true
date: 2007-05-15 04:00:00+00:00
layout: post
slug: creating-a-kml-feed-from-flickr-using-yahoo-pipes
title: Creating A KML Feed From Flickr Using Yahoo! Pipes
wordpress_id: 32
categories:
- Photography
---

I’ve written [a lot](http://www.strandbygaard.net/2007/05/11/workflows-for-geo-tagging-digital-photographs-part-1/) [about](http://www.strandbygaard.net/2007/05/11/workflows-for-geo-tagging-digital-photographs-part-2/) [geotagging](http://www.strandbygaard.net/2007/05/14/workflows-for-geo-tagging-digital-photographs-part-3/) images. One of the main purposes of doing this is to be able to search and display images in new ways, e.g. by placing the images on a map.

Services like [Google Maps](http://maps.google.com/), [Flickr](http://www.flickr.com/), Zoomr, and many others will plot your images on a map in a browser, but as map application goes nothing, in my opinion, beats [Google Earth](http://earth.google.com/).

One very easy way of plotting images from Flickr on Google Earth is using [Yahoo!](http://www.yahoo.com/) [Pipes](http://pipes.yahoo.com/) which offers "native" support for outputting data as KML. It’s so clever that even Google, has written an article on [how to do it](http://googlemapsapi.blogspot.com/2007/04/introduction-and-yahoo-pipes.html).

Yahoo! Pipes is a very cool service allowing data manipulation processes that work on data on the Internet, to be created using drawing tools, but this description doesn’t quite do justice to this extremely innovative service, so I suggest taking a longer look.

Taking an image feed from Flickr and transforming it into a (network linked) KML file that can be displayed in Google Earth is performed in three simple steps, and one image says it all.

[This](http://pipes.yahoo.com/pipes/pipe.run?_id=ODL51xUD3BGNlb6OJZhxuA&_render=kml) is the resulting KML file. Just add "&_render=kml" to the resulting feed from the pipe.

[![Example Pipes Application](http://www.strandbygaard.net/wp-content/uploads/2007/06/creating-a-kml-feed-from-flickr-using-yahoo-pipes.png)](http://www.strandbygaard.net/wp-content/uploads/2007/06/creating-a-kml-feed-from-flickr-using-yahoo-pipes.png)