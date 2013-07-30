---
author: Martin Strandbygaard
comments: true
date: 2007-05-11 04:00:00+00:00
layout: post
slug: workflows-for-geo-tagging-digital-photographs-part-2
title: 'Workflows for Geo-Tagging Digital Photographs (part 2)'
wordpress_id: 29
categories:
- Photography
tags: [RAW, GPS, Geotagging]
---

### Manual Geo-Tagging Digital Images

The cheapest solution to geo-tag images is to manually select the location where the images where taken in a map application such as [Google Maps](http://maps.google.com/) or [Google Earth](http://www.strandbygaard.net/;http://earth.google.com%22), and update the EXIF date in the image with the coordinates of the selected location. This approach works really well if the images are shot in a limited number of locations, and those locations are easily identifiable in a map location.

Finding the exact location in a map application where an image was shot is tedious work, even more so than assigning keywords (we all do that meticulously for all our images, right?), hence if the images are shot in many different locations, (at least) I quickly tire of using this approach. That may just be a limitation of my patience (which is generally pretty good), or the time I can spare for this type of work, so your experience may differ.

The speed with which the location can be determined with an acceptable degree of precision in a map application, closely relates to this. If images portray easily identifiable (at a distance) buildings or landmarks, then finding those locations in a map application becomes much easier than identifying points on a trail from a 10 kilometer hike.

One situation where this approach does work really well, is if images are shot indoors. A GPS device wouldn’t work indoors anyway, so this becomes the only approach, and the geographical "spread" of buildings is limited (compared to the 10 kilometer hike), so it’s generally enough to identify all images within the same building by just one coordinate.

### A Note On Precision

It may be tempting to try to determine the shooting location with the best possible precision, however I would suggest not to. Using a GPS to determine the shooting location will only give a precision of at most 10m, and coordinates obtained from a map application are also only about to within 10m (you need to use a "real" GIS application to get closer than that), so a 10m precision is in my opinion the closest you should aim for.

However, the real question is, what degree of precision do you really need? In some cases, the exact location (to within 10m) is desireable, but in other cases if +/- 200km is the best you can get, then isn’t that better than not having the location at all?

### The Right Tools For The Job

Not so long ago, there were almost no tools to do this; not so anymore. In my first workflow for geo-tagging images, I extracted the coordinates from Google Earth, and scripted [exiftool](http://www.sno.phy.queensu.ca/%7Ephil/exiftool/) to batch update the EXIF tag in images. This quickly evolved to bringing along a GPS device, and matching timestamps between the GPS track log and the images, which I’ll write about in the next part. Within the last 6 months, a plethora of tools to do this in a more userfriendly way have appeared.

On Mac OS X, I’ve used: 

  * [Geotagger](http://craig.stanton.net.nz/software/Geotagger.html) (my current favorite)
  * [PhotoGPSEditor](http://www.mmisoftware.co.uk/pages/photogpseditor.phphttp://www.mmisoftware.co.uk/pages/photogpseditor.php) (looks nice, but it never really suited my workflow)
  * [iPhotoToGoogleEarth](http://craig.stanton.net.nz/software/iPhotoToGoogleEarth.html) (please make one for Aperture/Lightroom)
  * [Geophoto](http://www.ovolab.com/geophoto/) (I haven’t tested this, but it looks nice)

On Windows I’ve noticed a few: 

  * [Google Picasa](http://picasa.google.com/) using [Google Earth](http://earth.google.com/) (works just like iPhotoToGoogleEarth)
  * [RoboGEO](http://www.robogeo.com/home/) (looks very nice, but I haven’t tested this)
  * [World Wide Media Exchange](http://wwmx.org/)
  * …. many others I’m sure

I’ve tested pretty much every tool I’ve come across that has to do with Geo-tagging, but in the end the solution that works best for me when manually geo-tagging images, is: Select a location in Google Earth (Use [this](http://www.ogleearth.com/crosshairs.kmz) placemark to put a nice crosshairs in the center of [Google Earth](http://earth.google.com/))

[![workflows-for-geo-tagging-digital-photographs-part-2_1.jpg](http://www.strandbygaard.net/wp-content/uploads/2007/06/workflows-for-geo-tagging-digital-photographs-part-2_1.jpg)](http://www.strandbygaard.net/wp-content/uploads/2007/06/workflows-for-geo-tagging-digital-photographs-part-2_1.jpg)

Select the images that were shot at that location

[![workflows-for-geo-tagging-digital-photographs-part-2_2.jpg](http://www.strandbygaard.net/wp-content/uploads/2007/06/workflows-for-geo-tagging-digital-photographs-part-2_2.jpg)](http://www.strandbygaard.net/wp-content/uploads/2007/06/workflows-for-geo-tagging-digital-photographs-part-2_2.jpg)

Drag the selected images to Geotagger

[![workflows-for-geo-tagging-digital-photographs-part-2_3.png](http://www.strandbygaard.net/wp-content/uploads/2007/06/workflows-for-geo-tagging-digital-photographs-part-2_3.png)](http://www.strandbygaard.net/wp-content/uploads/2007/06/workflows-for-geo-tagging-digital-photographs-part-2_3.png)

_In the next part, I’ll cover how to use the track log of a GPS device to match the recorded coordinates and images based on the EXIF time stamp, and have the coordinate add to the image as an EXIF tag …._
