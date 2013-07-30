---
author: Martin Strandbygaard
comments: true
date: 2007-05-30 04:00:00+00:00
layout: post
slug: a-more-advanced-how-to-name-and-store-digital-images
title: (A More Advanced) How To Name And Store Digital Images
wordpress_id: 35
categories:
- Photography
---

I’ve previously described [a simple workflow](http://www.strandbygaard.net/2007/05/10/how-to-name-and-store-digital-images/) for basic organization of digital images. Several people wrote me and asked if "that’s it" and why I don’t structure the process of assigning keywords (meta data). I think I covered the latter [here](http://www.strandbygaard.net/2007/05/26/how-to-select-keywords-for-photographs/), and in all fairness the workflow I described in my previous post "wasn’t it".

### The Workflow

I use a two-part workflow, in which I first store as much meta data in the image files as makes sense, and then import the image files in my image organizer of choice.
	
  1. Ingest images using importer of choice
  2. Rename files as "yyyymmdd-hhmmssss"
  3. Store in dated folders matching date of capture
  4. Batch assign as many IPTC fields as possible, including IPTC keywords
  5. Assign as many XMP fields as possible
  6. Store both IPTC and XMP within the files
  7. Import images into image organizer of choice
  8. Delete rejects
  9. Stack similar images
  10. Rate (1-3) the best images
  11. Assign more batch keywords
  12. Assign specific keywords to the rated images

### The Reason

Vendor lock in is one of the biggest problems of existing image organizers such as iPhoto, Aperture, and Lightroom _because they store image meta data outside the image file_. Consequently, the best way of locking all your images to one program and possibly one platform is by mindlessly using one of these programs.

On the other hand, these programs and indeed their approach to storing meta data has some great strengths that _I_ certainly want to leverage, so I’ve tailored a workflow that represents the best compromise I could device (according to my personal needs and preferences).

The two main requirements I’ve identified are:

  * Store all critical meta data in the image files
  * Manage all image files using the image organizer

To achieve this, I’m willing to accept that:

  * Meta data stored in the image files can only be updated outside the image organizer
  * Additional meta data added inside the image organizer is "lost"

And this corresponds to the two sections in my workflow. First, working directly with the image files, I add as much meta data as I can, and then using the image organizer I work through the images selecting keepers and rejects, rating them, and adding specific keywords to individual images.

### The Means

Many tools will do the job(s). I’m currently evaluating [Photo Mechanic](http://www.camerabits.com/), which looks to be the most promising choice for adding IPTC and IPTC4XMP meta data to images.

On Windows I really like [Breeze Browser Pro](http://www.breezesys.com/), which basically does what Photo Mechanic does, but at half the price and in some cases (e.g. IPTC categories) better.