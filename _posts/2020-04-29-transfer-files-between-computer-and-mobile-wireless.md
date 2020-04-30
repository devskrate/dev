---
layout: post
title:  "Transfer Files between PC and mobile wireless using QR code"
author: puneeth
categories: [ linux, file, dev-linux ]
image: assets/images/dev/linux/qrcp.png
tags: [linux, pc, windows, mobile]
---

Sometimes many of us face difficulty to transfer files from PC to mobile or from mobile to PC. It is a very annoying thing to use a cable for transferring a single file like an image or a small pdf. So here comes a small but a great tool used to transfer files over a network.

![QR image]({{ site.baseurl }}/assets/images/dev/linux/qrcp-qr.png){:height="60%" width="55%"}

To install this in linux follow the below steps
``` batch
go get github.com/claudiodangelis/qrcp
cd go/qrcp/bin
sudo mv qrcp /usr/local/bin
sudo chmod +x /usr/local/bin/qrcp
```
To send a file from pc to mobile
``` batch
qrcp MyDocument.pdf
```

To receive a file
```batch
qrcp receive
```
scan the code and you will be directed to an upload page.

![qrcp demo]({{ site.baseurl }}/assets/images/dev/linux/qrcp-demo.gif){:height="60%" width="55%"}

![qrcp demo]({{ site.baseurl }}/assets/images/dev/linux/qrcp-mobile-demo.gif){:height="60%" width="55%"}

For more details of how to use it and installation in other platforms visit: [qrcp](https://github.com/claudiodangelis/qrcp)

source: [Dev Useful Stuff](t.me/dev_useful_stuff)

**Additional info**: This is an open-source project written in Golang. This project is cloned and build by others in python named [qr-filetransfer](https://github.com/sdushantha/qr-filetransfer).
