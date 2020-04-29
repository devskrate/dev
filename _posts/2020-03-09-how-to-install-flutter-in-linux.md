---
layout: post
title:  "How to install Flutter in linux and Fix general problems"
author: puneeth
categories: [ windows, linux, os, tutorial, dev-linux ]
image: assets/images/flutter.png
tags: [os, linux, windows, student, google]
---

## Get the Flutter SDK

**1.** First clone the SDK from
<div class="highlight highlighter-rouge">
<div class="code-excerpt__code "><button class="code-excerpt__copy-btn btn" type="button" data-toggle="tooltip" title="" data-clipboard-text="git clone https://github.com/flutter/flutter.git -b stable" data-original-title="Copy code">  <i class="material-icons">content_copy</i></button>
<pre class="highlight">

<code><span class="gp">$</span> git clone https://github.com/flutter/flutter.git -b stable 
</code></pre>
</div>
</div>

**2.** Now, extract it in the desired location(preferred 'home' directory) by either right clicking and extract or by 
<div class="highlight highlighter-rouge">
<div class="code-excerpt__code "><button class="code-excerpt__copy-btn btn" type="button" data-toggle="tooltip" title="" data-clipboard-text="tar xf flutter_linux_v1.12.13+hotfix.8-stable.tar.xz" data-original-title="Copy code">  <i class="material-icons">content_copy</i></button>
<pre class="highlight">

<code><span class="gp">$</span> tar xf flutter_linux_v1.12.13+hotfix.8-stable.tar.xz
</code></pre>
</div>
</div>

**3.** Now add flutter to your PATH
<div class="highlight highlighter-rouge">
<div class="code-excerpt__code "><button class="code-excerpt__copy-btn btn" type="button" data-toggle="tooltip" title="" data-clipboard-text='export PATH="$PATH:`pwd`/flutter/bin"' data-original-title="Copy code">  <i class="material-icons">content_copy</i></button>
<pre class="highlight">

<code><span class="gp">$</span> export PATH="$PATH:`pwd`/flutter/bin"
</code></pre>
</div>
</div>

**4.** The last step is running
<div class="highlight highlighter-rouge">
<div class="code-excerpt__code "><button class="code-excerpt__copy-btn btn" type="button" data-toggle="tooltip" title="" data-clipboard-text="flutter doctor" data-original-title="Copy code">  <i class="material-icons">content_copy</i></button>
<pre class="highlight">

<code><span class="gp">$</span> flutter doctor
</code></pre>
</div>
</div>

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

![Android-studio-settings-sdk]({{ site.baseurl }}/assets/images/android/flutter-install-1.png)
**2.** Now UNCHECK the "Hide Obsolete packages" and then verify all the below mentioned are installed.
+ Android SDK Build-Tools
+ Android SDK Command-line Tools
+ Android SDK Platform-Tools
+ Android SDK Tools(Obsolete) [This is generally hidden until you uncheck the Hide Obsolete Packages]

![Android-SDK-Tools(Obsolete)-Install]({{ site.baseurl}}/assets/images/android/flutter-install-2.png)
Install(Tick all the above and click apply, wait until download and installation of the above packages) the above packages.

Then, goto Terminal and run
<div class="highlight highlighter-rouge">
<div class="code-excerpt__code "><button class="code-excerpt__copy-btn btn" type="button" data-toggle="tooltip" title="" data-clipboard-text="flutter doctor" data-original-title="Copy code">  <i class="material-icons">content_copy</i></button>
<pre class="highlight">

<code><span class="gp">$</span> flutter doctor
</code></pre>
</div>
</div>

By this time it should work. If it is not working close and open the terminal and set the PATH and try again.
