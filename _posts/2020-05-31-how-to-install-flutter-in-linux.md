---
date: 2020-05-31 16:26:40
layout: post
title: How to install Flutter in linux and Fix general problems
subtitle: Flutter installation
description: Flutter installation and fixing common problems and errors
image: https://devskrate.github.io/assets/blog-banners/flutter-installation.jpg
optimized_image: https://devskrate.github.io/assets/blog-banners/optimized/flutter-installation.webp
category: [dev]
tags: [os, linux, windows, student, google]
author: puneeth
---

## Get the Flutter SDK

**1.** First clone the SDK from

```bash
git clone https://github.com/flutter/flutter.git -b stable
```

**2.** Now, extract it in the desired location(preferred 'home' directory) by either right clicking and extract or by

```bash
tar xf flutter_linux_v1.12.13+hotfix.8-stable.tar.xz
```

**3.** Now add flutter to your PATH

```bash
export PATH="$PATH:`pwd`/flutter/bin"
```

**4.** The last step is running

```bash
flutter doctor
```

This command checks your environment and displays a report to the terminal window. The Dart SDK is bundled with Flutter; it is not necessary to install Dart separately. Check the output carefully for other software you might need to install or further tasks to perform (shown in bold text).

**Note: Android studio is mandatory for running Flutter**

##### After this many people may face issues with android studio. For example like this

```
[-] Android toolchain - develop for Android devices
    • Android SDK at /Users/obiwan/Library/Android/sdk
    ✗ Android SDK is missing command line tools; download from https://goo.gl/XxQghQ
    • Try re-installing or updating your Android SDK,
      visit https://flutter.dev/setup/#android-setup for detailed instructions.
```

#### To, resolve these issues even after installing Android studio, follow the below steps

**1.** Open android studio and then goto settings and then Android SDK.

<a href="https://devskrate.github.io/assets/images/android/flutter-install-1.webp" data-lightbox="image-2" data-title="Android-studio-settings-sdk"><img width="" src="https://devskrate.github.io/assets/images/android/flutter-install-1.webp" alt="Android-studio-settings-sdk"></a>

**2.** Now UNCHECK the "Hide Obsolete packages" and then verify all the below mentioned are installed.

- Android SDK Build-Tools
- Android SDK Command-line Tools
- Android SDK Platform-Tools
- Android SDK Tools(Obsolete) [This is generally hidden until you uncheck the Hide Obsolete Packages]

<a href="https://devskrate.github.io/assets/images/android/flutter-install-2.webp" data-lightbox="image-2" data-title="Android-SDK-Tools(Obsolete)-Install"><img width="" src="https://devskrate.github.io/assets/images/android/flutter-install-2.webp" alt="Android-SDK-Tools(Obsolete)-Install"></a>

Install(Tick all the above and click apply, wait until download and installation of the above packages) the above packages.

Then, goto Terminal and run

```bash
flutter doctor
```

By this time it should work. If it is not working close and open the terminal and set the PATH and try again.
