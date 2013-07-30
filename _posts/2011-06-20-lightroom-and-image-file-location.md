---
author: strandbygaard
comments: true
date: 2011-06-20 04:00:14+00:00
layout: post
slug: lightroom-and-image-file-location
title: Lightroom and Image File Location
wordpress_id: 167
categories:
- Photography
tags:
- Lightroom
- Dropbox
---

If you only use a Lightroom catalog on a single computer, the requirements for storing the image files aren't that complicated, but how to do it, if the same image catalog is to be used on many different computers?

I've previously written a long [post](http://blog.strandbygaard.net/2011/06/16/lightroom-and-dropbox-heres-how-to-do-it/) about using [Dropbox](www.dropbox.com) to sync a Lightroom catalog between multiple computers so Dropbox may seem like the obvious answer, but for storing actual image files, I don't think it is.

Here's how I do it. I store all originals on a NAS (with raid protection, multiple backups, etc.) on my home network, and then link to the image files in Lightroom using their UNC network path, e.g. `\\\path\to\image.dng`.

The advantage of doing this, in relation to the Lightroom catalog, is that this solution is platform independent. I use Lightroom on both Windows and Mac, and the UNC network path is the same on both platforms. 

If I'd referenced the images using a mapped network drive on Windows (e.g. `Z:\path\to\image.dng`), then they wouldn't be accessible in Lightroom on Mac, as a Mac doesn't know what 'Z:' means. It would also mean that this network path must map to the same drive letter all the time, and on all Windows computers, where Ligthroom is to be used, which is also a chore.

There's a slight quirk in Ligthroom when using UNC network paths to store image files. Lightroom is case sensitive about the path, so `\\host\path\to\image` and `\\HOST\path\to\image` will end up as two _different_ locations in Lightroom, although they're obviously not. This seems more like a bug than a feature.

By using the UNC network path, the original images are available in Lightroom on any platforms so long as this network path is available, includng using a VPN connection when I'm not at home.

As an added aside, it makes upgrading computers much easier as you don't have to safely transfer hundreds of gigabytes of image files, and you don't have to re-link tens or hundreds of folders in the catalog, because the image file location has changed. Remember when the users' home directory location in Windows changed from `'Documents and Settings'` to `'Users'` ...
