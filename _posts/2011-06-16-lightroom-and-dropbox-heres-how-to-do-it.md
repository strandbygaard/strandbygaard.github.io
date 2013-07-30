---
author: strandbygaard
comments: true
date: 2011-06-16 04:00:36+00:00
layout: post
slug: lightroom-and-dropbox-heres-how-to-do-it
title: Lightroom and Dropbox - Here's how to do it
wordpress_id: 158
categories:
- Photography
tags:
- Lightroom
- Dropbox
---

I've finally found a simple solution to using the same Lightroom image catalog on multiple computers: Store the Lightroom catalog, settings, plugins, and previews in a folder in [Dropbox](http://www.dropbox.com), and magic happens. 

The only caveat is that you _must_ wait for Dropbox to complete synchronization when switching from one computer to another.

I've been using Lightroom for a long time. [Here's why](http://blog.strandbygaard.net/2007/09/10/the-only-reason-needed-to-choose-lightroom/).

Accessing the same image catalog on different computers, e.g. a laptop and a desktop has always been a frustrating experience. I use just a single image catalog, and I need access to this catalog both on my laptop when I'm working with a client and on my desktop, when I'm working at home.

Note that I don't need access to the originals, I just need access to the catalog and previews, and I need to be able to update the catalogue.

I've tried many different solutions, but they've all been flawed in one of two ways. They've either been too slow, e.g. using rsync to keep multiple copies in sync, or not offered any seeamless backup protection of the catalog, e.g. storing the catalog on an external portable drive.

This problem obviously applies to most image cataloging software, like Aperture, iPhoto, and iView Media Pro (now Microsoft). The only notable exception has been Google Picasa, which for a long time has offered to sync images between multiple computers using Picasaweb as intermediary.

Here's how to do it:
	
  1. Create a folder within the dropbox folder. I created a folder 'Lightroom' under the photos folder in Dropbox, but any folder will work
  2. Copy everything from the old Lightroom folder, to this new folder location
  3. Let Dropbox complete the syncronization
  4. Open the copied Lightroom catalog, and verify that everything works just as before
  5. Change Lightroom preferences, so that it stores user presets in a folder. Lightroom defaults to storing user presets in the user's home directory (that would be %APPDATA% on windows), but we want these available on all computers where Lightroom is used
  6. Optional, but highly recommended: Change Lightroom preferences to update metadata in originals

Most people I've found writing about this suggest that you set Lightroom to delete fullsize previews after a very short time, e.g. one day, to reduce the size of the previews folder. I don't think this is a general recommendation, because it's mostly a trade off in terms of speed. Whether or not it's a good idea depends on two things: Do you actually need the fullsize previews, and what kind of Internet connectivity do you have?

If you need the fullsize previews badly enough, then you're probably willing to accept the storage overhead, and the delay caused by syncing them, and after initial sync, this isn't going to be that much anyway. On the other hand, if you don't need them, you might as well not store them, to save space and gain a little speed.

I don't need them, so I don't store them for very long, but I do set my standard preview size quite large, which actually adds up to a bigger storage overhead than keeping smaller standard size previews, and storing fullsize previews for a longer period of time.

Next up is a post on how to store the actual image files ...
