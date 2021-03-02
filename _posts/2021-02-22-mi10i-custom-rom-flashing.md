---
date: 2021-02-22 09:26:40
layout: post
title: Mi 10i any Custom Rom flashing guide.
subtitle: "Mi 10i ArrowOS, PixelExperience, dotOS, LineageOS, ResurrectionRemix, ProjectSakura, exTHmUI"
description: >-
  Customs roms are very usefull especially for old devices and Xiaomi phones, as miui is bundled with ads. Here we install ArrowOS in Mi 10i.
image: >-
  https://devskrate.github.io/assets/blog-banners/flash-custom-rom-in-mi-10i.jpg
optimized_image: >-
  https://devskrate.github.io/assets/blog-banners/optimized/flash-custom-rom-in-mi-10i.webp
category: [mobiles]
tags: [arrowos, customrom, mi, xioami, gsi]
author: puneeth
is_generated: false
---

For flashing any custom rom your phone bootloader should be unlocked and should have a Recovery. So first unlock Mi 10i bootloader. If you have not yet unlocked Mi 10i bootloader, then first unlock bootloader of any xiaomi device by following this [link](https://mobie.tech/unlock-bootloader-of-any-xiaomi-phone/)

ArrowOS Download link : [https://downloads.arrowos.net/gauguin](https://downloads.arrowos.net/gauguin)


Code name of Mi 10i, Redmi Note 9 Pro 5G & Mi 10T Lite : **gauguin**
Codename changes with region, but **gauguin** is common.

Three devices are similar and released with different names in different markets, only the differences are
+ Mi 10i is exactly same as Redmi Note 9 Pro 5G, just a rebranding.
+ Mi 10T Lite has 64 MP Sony IMX682 sensor & Redmi Note 9 Pro 5G / Mi 10i has 108 MP Samsung HM2 sensor.

>Note: Flashing CustomRom will erase the data, so backup your data.

There are 2 ways for flashing custom rom based on the rom you are,

### 1. For those who are on AOSP Custom ROM:

+ Wipe Dalvik/ART Cache, Cache & Data.
+ Flash ROM.
+ Flash GApps (for Vanilla ROM).
+ Format data. (Take backup of your data before doing this).
    - TWRP: Wipe > Format Data
    - OFOX: Menu > Manage Partitions > Data > Format Data
+ Reboot.


### 2. For those who are on any MIUI:

+ Flash or update to latest stock MIUI 12 for your device variant.
>Ignore above step if you are already on latest stock MIUI 12 for your device variant. 

+ Wipe Dalvik/ART Cache, Cache & Data.
+ Flash ROM.
+ Flash GApps (for Vanilla ROM).
+ Format data. (Take backup of your data before doing this).
    - TWRP: Wipe > Format Data
    - OFOX: Menu > Manage Partitions > Data > Format Data
+ Reboot.


### 3. Flashing an update to an UnOfficial Custom Rom(Dirty Flash):

+ Wipe Dalvik/ART Cache & Cache.
+ Flash ROM.
+ Reboot.