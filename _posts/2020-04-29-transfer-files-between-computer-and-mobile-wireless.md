---
date: 2020-04-29 17:26:40
layout: post
title: "Transfer Files between PC and mobile wireless using QR code"
subtitle: Easy transfer files between pc an mobile
description: >-
  An easy way to transfer files between pc snd mobile with just scanning qr code.
image: https://devskrate.github.io/assets/blog-banners/file-transfer-qr.jpg
optimized_image: https://devskrate.github.io/assets/blog-banners/optimized/file-transfer-qr.webp
category: [dev]
tags: [linux, pc, windows, mobile]
author: puneeth
paginate: false
is_generated: false
---

Sometimes many of us face difficulty to transfer files from PC to mobile or from mobile to PC. It is a very annoying thing to use a cable for transferring a single file like an image or a small pdf. So here comes a small but a great tool used to transfer files over a network.

![QR image](https://devskrate.github.io/assets/images/dev/linux/qrcp-qr.png){:height="60%" width="55%"}

To install this in linux follow the below steps

```batch
go get github.com/claudiodangelis/qrcp
cd go/qrcp/bin
sudo mv qrcp /usr/local/bin
sudo chmod +x /usr/local/bin/qrcp
```

To send a file from pc to mobile

```batch
qrcp MyDocument.pdf
```

To receive a file

```batch
qrcp receive
```

scan the code and you will be directed to an upload page.

<img style="display: inline;" src="https://devskrate.github.io/assets/images/dev/linux/qrcp-demo.gif" width="55%" height="60%">
<img style="display: inline;" src="https://devskrate.github.io/assets/images/dev/linux/qrcp-mobile-demo.gif" width="55%" height="60%">

For more details of how to use it and installation in other platforms visit: [qrcp](https://github.com/claudiodangelis/qrcp)

source: [Dev Useful Stuff](https://t.me/dev_useful_stuff)

**Additional info**: This is an open-source project written in Golang. This project is cloned and build by others in python named [qr-filetransfer](https://github.com/sdushantha/qr-filetransfer).
