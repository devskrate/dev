---
date: 2020-03-30 17:26:40
layout: post
title: "Install Google Chrome in Ubuntu/Linux"
subtitle: Installing chrome ein ubuntu and other linux
description: >-
  There are 2 methods to install in linux. 1st is from downloading manually as in windows and the 2nd is with commands.
image: https://devskrate.github.io/assets/blog-banners/chrome-in-linux.jpg
optimized_image: https://devskrate.github.io/assets/blog-banners/optimized/chrome-in-linux.webp
category: [howto]
tags: [linux, pc, operating system, chrome, google]
author: puneeth
paginate: false
is_generated: false
---

Google chrome is one of the most used popular browsers.

Firefox has improved a lot lately and is a better choice specially from the privacy point of view. However, if you are an ardent fan of Google Chrome, I won’t force you to ditch Chrome and move to Firefox.

Ofcourse chrome is available for linux, but Google Chrome is not an open source and if you try to install Google Chrome from Ubuntu Software Center, you won’t find it there. It will probably suggest installing Chromium (the open source project Chrome is derived from). Chromium is similar to Chrome but it’s still not the real Google Chrome.. Now, we will see the installation of google chrome.

There are two methods to install Google Chrome.

1. Graphical install
2. Command line install

#### 1. Graphical method [Begginer's method]

If you are new to ubuntu and Linux world, this method is preferable(If you interested in administration, you can give a try with command line)
Firstly go to the official website for downloading chrome.

<a href="https://www.google.com/chrome/" target="_blank"><button style="cursor: pointer; color: whitesmoke; background-color: black; display: inline-block;text-decoration: none; border: none; max-width: 100%; font-size:20px">Download Google chrome
</button></a>

You will see a download link there, now click the "Download chrome" button to download.

<img src="https://devskrate.github.io/assets/images/linux/chrome-download.webp" alt="Chrome download page" style="max-width: 100%; border:0;"/>

Now, you can see tat it is asking to select between two versions.

<img src="https://devskrate.github.io/assets/images/linux/chrome-select.webp" alt="Chrome download page" style="max-width: 100%; border:0;"/>

If you want to install chrome for other linux systems like Fedora, openSUSE download the "rpm package", but we are now installing it for Ubuntu, download the ubuntu package.

After downloading, open the downloaded file by double clicking it. Now,Ubuntu software center is opened and chrome will be staged for installation.

<img src="https://devskrate.github.io/assets/images/linux/chrome-install.webp" alt="Chrome download page" style="max-width: 100%; border:0;"/>

Now, just press "install", google chrome will be installed.

### 2. Command line Method (Advanced or Interested user's)

This process is generally annoying for begginer users. So, follow the below steps carefully.

To install chrome we need to download it.

```
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
```

Type the command in he terminal

After the download process is finised, try to install it using the following command in the directory where you have downloaded

```
sudo dpkg -i google-chrome-stable_current_amd64.deb
```

That's it, your system will be installed with chrome!!
Coming to updating the chrome, you can update it while you are updatong your systems.
