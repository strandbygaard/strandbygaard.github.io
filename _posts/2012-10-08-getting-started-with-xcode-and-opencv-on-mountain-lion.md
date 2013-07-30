---
author: strandbygaard
comments: true
date: 2012-10-08 15:59:45+00:00
layout: post
slug: getting-started-with-xcode-and-opencv-on-mountain-lion
title: Getting Started With XCode And OpenCV On Mountain Lion
wordpress_id: 235
categories:
- Development
tags: [OpenCV]
---

Ever tried getting [OpenCV](http://www.opencv.org) running in Mac OS X 10.8 (Mountain Lion)?

Plowing through all the documentation and guides can be a pretty daunting task (well, at least they exist). These simple steps will get you up and running with OpenCV 2.4.2 in XCode 4.5:

First compile, build, and install OpenCV from sources:
	
  1. Install [Homebrew](http://mxcl.github.com/homebrew/). Open Terminal, and run this command `ruby -e "$(curl -fsSkL raw.github.com/mxcl/homebrew/go)"`
  2. Run `brew install` with all of {svn, cmake, ffmpeg, libjpeg, libpng }
  3. Get the latest sources for OpenCV (currently OpenCV 2.4.2) [here](http://opencv.org/)
  4. Unpack somewhere and cd into the folder in Terminal
  5. Run `cmake .`
  6. Run `make && make install`

Next step is to create an XCode project that uses OpenCV. This is as simple as creating a new C/C++ project and specifying search path for the OpenCV headers and libraries:
	
  1. Open XCode and choose `File > New > Project > Command Line Tool`
  2. For the target select `Build Settings`
  3. For Header Search Paths, specify `/usr/local/include`
  4. For Library Search Paths, specify `/usr/local/lib`

In main.cpp, add something like this to test it out:

``` cpp
#include <opencv2/opencv.hpp>

int main(int argc, char *argv[])
{
    IplImage *img = cvCreateImage( cvSize(100,200), IPL_DEPTH_8U, 3);
    cvNamedWindow("Hello World!", CV_WINDOW_AUTOSIZE);
    cvShowImage("Hello World!", img);
    cvWaitKey(0);
    cvDestroyWindow("Hello World!");
    cvReleaseImage(&img);

    return 0;
}
```
An alternative method is to install OpenCV with Homebrew, `brew install opencv` (not tested), but the dependencies requires amongst other things a fortran compiler, which I didn't want on my system, so I took the slightly more elaborate approach of manually installing dependencies and building OpenCV from source. 

Edit:

See also this [guide](http://opencv.willowgarage.com/wiki/UsingOpenCVUnderOSX).
