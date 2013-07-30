---
author: Martin Strandbygaard
comments: true
date: 2007-05-01 04:00:00+00:00
layout: post
slug: fixing-the-windows-keyboard-layout-switching-bug
title: Fixing The Windows Keyboard Layout Switching Bug
wordpress_id: 27
categories:
- General
tags:
- dvorak
---

### The Solution

The Language Bar has user definable keyboard shortcuts for switching between defined keyboard layouts. Remove shortcuts for switching between layouts, and problem disappears. To get the following dialog, choose: `Start -> Settings -> Control Panel -> Regional And Language Options -> Languages Tab -> Details`

![](/images/2007-05-01-fixing-the-windows-keyboard-layout-switching-bug/language-bar-1.png)

Under the _Preferences_ section choose _Key Settings_ and here you can assign keyboard shortcuts related to keyboard layouts.

![](/images/2007-05-01-fixing-the-windows-keyboard-layout-switching-bug/language-bar-2.png)

### The Problem

Anyone using multiple keyboard layouts in Windows, will know that Windows has a seemingly magic feature whereby the keyboard layouts will switch at seemingly random times. One minute you’re typing using one layout and the next minute, or even mid-sentence, the layout will have changed and you’ll be typing gibberish.

Granted, the outcome does depend on the difference between the layouts, but if you’re using Dvorak and the other option is Qwerty then the result isn’t meaningful. Subjectively, the issues seems most prevalent after having changed layout settings, e.g. if you’ve just installed and switched to a custom layout, such as a Dvorak layout modified to support local language characters (Danish has three).

Until recently, I combated this issue by removing the Qwerty completely, but that doesn’t really work that well if your colleagues should have a decent chance at using your computer (but it does work wonders for the learning process for anyone new to Dvorak).