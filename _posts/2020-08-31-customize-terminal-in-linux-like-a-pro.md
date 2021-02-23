---
date: 2020-08-31 12:26:40
layout: post
title: How to customize your terminal like a developer and pro
subtitle: "Turn your Terminal like a pro"
description: >-
  Generally the terminals that we get from the different linux distributions are good but the only thing is, they are not good looking.
image: >-
  https://devskrate.github.io/assets/blog-banners/customize-linux-terminal-like-a-pro.jpg
optimized_image: >-
  https://devskrate.github.io/assets/blog-banners/optimized/customize-linux-terminal-like-a-pro.webp
category: [dev]
tags: [terminal, linux, pro, debian, terminator]
author: puneeth
is_generated: false
---

Generally the terminals that we get from the different linux distributions are good but the only thing is, they are not good looking. Actually they are nice but lack some details that most of them like to have. 

Here we will show you how to install most popular themes for your terminal..

Some of the popular tools to install themes are 
+ Ohmyzsh
+ Ohmyfish

In both of the above mentioned tools, we prefer ohmyfish because it has more good themes compared to ohmyzsh. If you want to install ohmyzsh, refer [this](https://devskrate.com/install-ohmyzsh-for-terminal/)

Let's see the installation of the Ohmyfish. Before actually using it in your default terminal try to apply on another terminal.

+ I use Gnome-Terminal as my default shell, to test this I downloaded **Terminator**. If you want to test it in terminator, then install terminator by `sudo apt install terminator`

+ Now check if you have `fish` installed in your system. Type `fish --version`. If you get a version number as response, then you have already installed it!. If you don't have it, install it using `sudo apt install fish`.

+ Now we need to install the Ohmyfish tool.. For that install the script by using any of the following method..
  - **Via direct curl**
    ```bash
      curl -L https://get.oh-my.fish | fish
      ```
      If you face errors from the above one, try to usee the below one.

  - **Via git**
      ```bash
      $ git clone https://github.com/oh-my-fish/oh-my-fish
      $ cd oh-my-fish
      $ bin/install --offline
      ```

Boom, you have just installed the tool! But you need more to do for customizing it..

+ Go to this link [https://github.com/oh-my-fish/oh-my-fish/blob/master/docs/Themes.md](https://github.com/oh-my-fish/oh-my-fish/blob/master/docs/Themes.md) and note down the name of the theme you like.

+ Now just type `omf install <theme-name>` in the terminal. 

+ After it is installed, type `omf theme <theme-name>`

+ **Note** :
Some of the themes may need [PowerLine Fonts](https://github.com/powerline/fonts). You can directly install it if you are in a Debian or Ubuntu based systems by `sudo apt-get install fonts-powerline`. 

Here are some of the themes that we use..

<div class="slide-show">

<a href="https://devskrate.github.io/assets/images/dev/terminal/ohmyfish-batman.png" data-lightbox="image-1" data-title="Ohmyfish Batman theme"><img width="85%" src="https://devskrate.github.io/assets/images/dev/terminal/ohmyfish-batman.png"></a>
<a href="https://devskrate.github.io/assets/images/dev/terminal/ohmyfish-bobthefish.png" data-lightbox="image-1" data-title="Ohmyfish Bobthefish theme"><img width="85%" src="https://devskrate.github.io/assets/images/dev/terminal/ohmyfish-bobthefish.png"></a>
<a href="https://devskrate.github.io/assets/images/dev/terminal/ohmyzsh-agnoster.jpg" data-lightbox="image-1" data-title="Ohmyzsh agnoster theme"><img width="85%" src="https://devskrate.github.io/assets/images/dev/terminal/ohmyzsh-agnoster.jpg"></a>


</div>

**Links for devs and interested (Misc)**:

- Ohmyfish : [https://github.com/oh-my-fish/oh-my-fish](https://github.com/oh-my-fish/oh-my-fish)
- PowerLineFonts : [https://github.com/powerline/fonts](https://github.com/powerline/fonts)
- Ohmyzsh : [https://github.com/ohmyzsh/ohmyzsh](https://github.com/ohmyzsh/ohmyzsh)