---
date: 2020-09-08 12:26:40
layout: post
title: How to downloadd windows10 lockscreen/spotlight images.
subtitle: "Download windows10 spotlight images"
description: >-
  The images shown in lockscreen of windows10 are really good, many want to get that pictures, so here is the way..
image: >-
  https://devskrate.github.io/assets/blog-banners/customize-linux-terminal-like-a-pro.jpg
optimized_image: >-
  https://devskrate.github.io/assets/blog-banners/optimized/customize-linux-terminal-like-a-pro.webp
category: [tips&tricks]
tags: [windows, windows10, spotlight, images, hack]
author: puneeth
is_generated: true
---

The images shown in lockscreen of windows10 are really good, many want to get that pictures. They are also called as spotlight pictures, so here is the way to get that pictures. 

### Find Windows Spotlight Lock Screen Pictures

Windows Spotlight Images are not stored in the most obvious of places. First, press `Windows key + R` then type: `%userprofile%` and hit Enter.

+ When File Explorer opens up, turn on Show hidden files and folders.
+ The AppData folder will now appear in your User folder. Open it then navigate to 
`Local > Packages > Microsoft.Windows.ContentDeliveryManager_cw5n1h2txyewy > LocalState > Assets`
+ The images will appear as blank files, with random names. Select all of them `Ctrl + a` then copy with `Ctrl + c`. Create a new folder where ever you like and then paste the files with `Ctrl + v`.
+ Open the folder containing the blank Files, click File menu > Open Command Prompt > Open Command Prompt as administrator.(Open CMD in the directory that you copied the pictures.)
+ Type the following command: `Ren *.* *.jpg` then hit Enter. This command will convert the blank files to JPEG images and make them visible.