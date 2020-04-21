---
layout: post
title:  "Some new Android 11 Features for developers"
author: puneeth
categories: [ android ]
image: assets/images/android11.png
tags: [google, android]
---

Android has led the way towards the future of mobile, with new technologies like 5G to foldable displays to machine learning built into the core. 

### 1. 5G experiences

5G brings consistently faster speeds and lower latency to more users around the world. With 5G you can extend your Wi-Fi app experiences -- such as streaming 4K video or loading higher-res game assets -- to mobile users, or you can build new experiences designed specifically for 5G.

+ **Dynamic meteredness API** - with this API you can check whether the connection is unmetered, and if so, offer higher resolution or quality that may use more data. The API to include cellular networks, so that you can identify users whose carriers are offering truly unmetered data while connected to the carrier’s 5G network. 
+ **Bandwidth estimator API** - API for 5G to make it easier to check the downstream/upstream bandwidth, without needing to poll the network or compute your own estimate. If the modem doesn’t provide support, we make a default estimation based on the current connection.

### 2. New screen types

Device makers like POCO, RealMe, Xiaomi, Nokia etc.. continuing to innovate by bringing exciting new form-factors and device screens to market. Extended support for these in the platform, with APIs to let you optimize your apps. 

+ **Pinhole and waterfall screens** - Apps can manage pinhole screens and waterfall screens using the existing display cutout APIs. If you want, a new API lets your app use the entire waterfall screen including the edges, with insets to help you manage interaction near the edges. 

### 3. Privacy

+ **Scoped storage** - Google continued it's work to better protect app and user data on external storage, and made further improvements to help developers migrate more easily. This preview release includes several enhancements, such as opt-in raw file path access for media, updated DocumentsUI, and batch edit operations in MediaStore. Along with these technical changes, based on your input, we are also giving you more time to make the migration and the changes will apply to your apps when they target Android 11.

### 4. Security 

+ **Biometrics** - It has expanded it's biometrics support to meet the needs of a wider range of devices. BiometricPrompt now supports three authenticator types with different levels of granularity -- strong, weak, and device credential. It also decoupled the BiometricPrompt flow from the app’s Activity lifecycle to make it easier to integrate with various app architectures, and to improve the transaction UI. All apps using biometric auth should move to the BiometricPrompt APIs, which are also available in AndroidX for compatibility with earlier versions of Android.
+ **Platform hardening** - It expanded use of compiler-based sanitizers in security-critical components, including BoundSan, IntSan, CFI, and Shadow-Call Stack. It is also enabling heap pointer tagging for apps targeting Android 11 or higher, to help apps catch memory issues in production. These hardening improvements may surface more repeatable/reproducible app crashes in your code. It has used HWAsan to find and fix many memory errors in the system, and it now offer HWAsan-enabled system images to help you find such issues in your apps.
+ **Secure storage and sharing of data** - Apps can now share data blobs easily and more safely with other apps through a BlobstoreManager. The Blob store is ideal for use-cases like sharing ML models among multiple apps for the same user.
+ **Identity credentials** - Android 11 adds platform support for secure storage and retrieval of verifiable identification documents, such as ISO 18013-5 compliant Mobile Driving Licenses.

### 5. App compatibility

+ **Easier testing and debugging** - To help you test for compatibility, it had made many of the breaking changes toggleable - meaning that you can force-enable or disable the changes individually from Developer options or adb. With this change, there’s no longer a need to change targetSdkVersion or recompile your app for basic testing. [ Check out the details here](https://developer.android.com/preview/test-changes).

<img src="{{ site.baseurl }}/assets/images/android/App-compatibility-toggles-in-Developer-Options.png" alt="App compatibility toggles in Developer Options" style="width:350px; border:0;"/> 

There are also Updated greylists, Dynamic resource loader, New platform stability milestone in the new preview.

There are some improvements in Connectivity like Call screening service improvements, Wi-Fi suggestion API enhancements, Passpoint enhancements and Image and camera improvements like HEIF animated drawables, Native image decoder, Muting during camera capture, Bokeh modes.

source: [ Turning it up to 11: the first Developer Preview of Android 11 ](https://android-developers.googleblog.com/2020/02/Android-11-developer-preview.html)