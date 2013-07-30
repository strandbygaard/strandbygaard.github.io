---
author: Martin Strandbygaard
comments: true
date: 2007-06-02 04:00:00+00:00
layout: post
slug: rediscovering-adobe-dng
title: Rediscovering Adobe DNG
wordpress_id: 37
categories:
- Photography
tags: [DNG]
---

Should RAW images be stored as that, or should they be converted to Adobe DNG? A seemingly very simple question, but with no easy answer unless looking in a crystal ball.

### Background

In short, each and every different digital camera model that can take pictures in RAW format does so in a different, proprietary, and undocumented format (pretty much). The result is more than 100 different RAW formats, some of which are no longer supported by the camera manufacturer.

The issue is little different from any other case of "proprietary vs. open format", but surprisingly while the world is severely divided on the question of Open Office XML (Microsoft) vs. Open Document Format (everyone else), everyone seem to agree that the "closed" and undocumented nature of current RAW formats will in time become a problem, as manufacturers seize support of older formats.

The discussion from here on becomes long and winded. Luminous Landscape has a [good article](http://www.luminous-landscape.com/essays/raw-flaw.shtml) on this specific issue, that has been dubbed "The Raw Flaw". [OpenRAW](http://www.openraw.org/) also has several articles on the problem, though I personally don’t believe in their solution.

Suffice it to say, if you also think it’s a problem you’ve probably at least contemplated possible solutions.

### The Difficult Decision

One such solution is the Adobe Digital Negative (DNG) format, which is Adobe’s attempt at a universal RAW standard. Much can be said about Adobe’s intentions for creating such a format, but it remains a fact that converting existing RAW formats to DNG removes "closed" and "proprietary" from the equation of file format support, and leaves just the issue of "support". Support in terms of selection of applications and time.

Adobe has made a serious commitment to this format, and combined with the relative difficulty of supporting an endless stream of new RAW formats, this has led to a fairly quick uptake by other application developers. By now all significant applications related digital imaging offer support for DNG.

This leaves just the question of support in time, hence the crystal ball. 5 years from now, will DNG have the better support? Or will hundreds of different RAW formats, most of which were used by cameras no longer in production, and most likely no longer in use?

Interestingly, there seems to be an almost automatic uptake of DNG amongst users of non- Nikon and Canon cameras as it’s generally accepted that there is greater risk that these manufacturers will exit the camera market space at some point.

With Nikon and Canon users the situation isn’t as clear cut as these companies carry much more weight and their significant user bases encompasses most professional photographers and will present a market in their own right for a very long time. In other words, just by looking at the numbers both Nikon and Canon RAW formats have significantly larger user bases, than DNG most likely has at this point in time (2007).


### Making A Decision

I’ve been looking at DNG on and off since it was released by Adobe, each time evaluating the functionality offered by [Adobe DNG Converter](http://www.adobe.com/products/dng/), and DNG support by the applications I use in [my workflow](http://www.strandbygaard.net/2007/05/30/a-more-advanced-how-to-name-and-store-digital-images/).

So far it hasn’t amounted to more than (a lot of) reading, doing a few large projects with DNG based workflows, and Aperture’s lack of support for XMP information in DNG, has kept me from considering DNG for a long time (because I insist on adding a lot of XMP metadata to the RAW files, but that’s likely an unusual requirement). However, while Aperture’s speed has improved significantly since it’s release, it appears that my patience with its lack thereof has declined more rapidly, and working with a Bridge CS3/Lightroom/Photoshop CS3 tool chain convinced me that it’s time for a major overhaul.

That also decision also suddenly reintroduced DNG as a viable option, and since I’ve decided I believe (and I think the question is reduced to that, a matter of belief) in a bright future for DNG, the were no more excuses to adopting it.

### Further Reading, Products, And Reviews

In my opinion the [Adobe DNG Converter](http://www.adobe.com/products/dng/) is the best RAW to DNG converter around. And they for the technically inclined, they also have the full [DNG specification](http://www.adobe.com/products/dng/pdfs/dng_spec.pdf) available.

Barry Pearson is an outspoken advocate of DNG, and his [website](http://www.barrypearson.co.uk/) has extensive information about everything DNG, including an extensive [list](http://www.barrypearson.co.uk/articles/dng/products.htm) of products supporting DNG. He also has different subsets of this list, e.g. a list of [products supporting DNG and embedded XMP](http://www.barrypearson.co.uk/articles/dng/xmp_dng.htm), which I think is a requisite to use a tool in a workflow.

Most big photo related websites have mentioned Adobe DNG at some point, so there are plenty of good [reviews and howto’s](http://www.adobe.com/products/dng/reviews.html) to be read. [Digital Outback Photo](http://www.outbackphoto.com/) has a very nice coverage on digital workflow, including a [good write up on Adobe DNG Converter](http://www.outbackphoto.com/artofraw/raw_17/essay.html). Luminous Landscape also has a [good commentary](http://www.luminous-landscape.com/reviews/software/dng.shtml) on it.