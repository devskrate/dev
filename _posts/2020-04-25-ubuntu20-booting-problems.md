---
layout: post
title:  "Ubuntu 20.04 booting problems." 
author: puneeth
categories: [ ubuntu, linux ]
image: assets/images/linux/ubuntu-clogo.jpg
tags: [ubuntu, linux, kernel, intel, os, featured]
---

Ubuntu 20.04 LTS has been released recently, after upgrading to it from ubuntu 18, 19, many had may faced booting problems(especially in DualBoot's).
Booting problems like bootloop(Restarting when ubuntu is selected) or blank screen after selecting ubuntu in the grub.

With My experience, I am giving here few fixes you may try.

**1. Uncheck the PPT security in BIOS**

Firstly goto the BIOS (It depends on the system, for Dell press F12), then goto security, then goto PTT security and Uncheck it.
```
Security -> PTT Security and uncheck PTT On
```
Click Apply (I would recommend choosing Save as Custom User Settings), then OK, then Exit.

This should acctuallly work. If this does not work, try the second method.

**2. Boot from Advanced Options**

While booting from grub, you can see "Advanced Options for Ubuntu". Select it and in that boot from the Old Kernel.
You may find many things like 
- Ubuntu, with Linux 5.4-generic
- Ubuntu, with Linux 5.4-generic (recovery mode)
- Ubuntu, with Linux 4.*-generic
- Ubuntu, with Linux 4.*-generic (recovery mode)

Boot with Linux 4.*-generic, don't boot with recovery or any other options availabe additionally.
Now, you will boot into Ubuntu:).

Remember, this method is not a permanent fix, you can use Ubuntu inthis way as long as you find the permanent fix, this will not do anything from accessing all the features.

**Additional Info**: Why method 2 is not a permanent fix, because Ubuntu uses Linux kernel 5.4, so grub will boot from it by default. After booting in you can change the default kernel to boot, but be carefull while handling with the Kernel.