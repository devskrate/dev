---
date: 2020-07-30 16:26:40
layout: post
title: How to customize your terminal like a developer using zsh
subtitle: "Turn your Terminal like a pro using zsh"
description: >-
  Customize terminal using zsh.
image: >-
  https://devskrate.github.io/assets/blog-banners/ohmyzsh-terminal-installation.jpg
optimized_image: >-
  https://devskrate.github.io/assets/blog-banners/optimized/ohmyzsh-terminal-installation.webp
category: [dev]
tags: [terminal, linux, pro, debian, terminator]
author: puneeth
is_generated: false
---

Let's see the installation of the Ohmyzsh. Before actually using it in your default terminal try to apply on another terminal.

+ I use Gnome-Terminal as my default shell, to test this I downloaded **Terminator**. If you want to test it in terminator, then install terminator by `sudo apt install terminator`
+ Now check if you have `zsh` installed in your system. Type `zsh --version`. If you get a version number as response, then you have already installed it!. If you don't have, install it by using `sudo apt install zsh`

+ Now we need to install the Ohmyzsh tool.. For that install the script by using any of the following method..
    - **Via curl**
    ```bash
    sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
    ```
    - **Via wget**
    ```bash
    sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
    ```
    - **Via fetch**
    ```bash
    sh -c "$(fetch -o - https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
    ```
Boom, you have just installed the theme! But you need more to do for customizing it..

+ Go to this link [https://github.com/ohmyzsh/ohmyzsh/wiki/Themes](https://github.com/ohmyzsh/ohmyzsh/wiki/Themes) and note down the name of the theme you like.

+ Now just type `nano ~/.zshrc` in the terminal. We are using nano editor for editing the `.zshrc` file. You can also use your own one's but recommended is nano.

+ You can see a line `ZSH_THEME="robbyrussell"`. Now in the place of `robbyrussell` or any other insert your theme name that you liked in the above step.

+ **Note** :
Some of the themes need [PowerLine Fonts](https://github.com/powerline/fonts). You can directly install it if you are in a Debian or Ubuntu based systems by `sudo apt-get install fonts-powerline`. 

Here are some of the themes that we use..

<div class="slide-show">

<a href="https://devskrate.github.io/assets/images/dev/terminal/ohmyzsh-agnoster.jpg" data-lightbox="image-1" data-title="Ohmyzsh agnoster theme"><img width="85%" src="https://devskrate.github.io/assets/images/dev/terminal/ohmyzsh-agnoster.jpg"></a>
<a href="https://devskrate.github.io/assets/images/dev/terminal/ohmyfish-batman.png" data-lightbox="image-1" data-title="Ohmyfish Batman theme"><img width="85%" src="https://devskrate.github.io/assets/images/dev/terminal/ohmyfish-batman.png"></a>
<a href="https://devskrate.github.io/assets/images/dev/terminal/ohmyfish-bobthefish.png" data-lightbox="image-1" data-title="Ohmyfish Bobthefish theme"><img width="85%" src="https://devskrate.github.io/assets/images/dev/terminal/ohmyfish-bobthefish.png"></a>

</div>

**Links for devs and interested**:

- Ohmyzsh : [https://github.com/ohmyzsh/ohmyzsh](https://github.com/ohmyzsh/ohmyzsh)
- PowerLineFonts : [https://github.com/powerline/fonts](https://github.com/powerline/fonts)
- Ohmyfish : [https://github.com/oh-my-fish/oh-my-fish](https://github.com/oh-my-fish/oh-my-fish)