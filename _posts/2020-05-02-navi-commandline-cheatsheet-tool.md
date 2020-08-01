---
date: 2020-05-02 9:14:07
layout: post
title: Navi - An interactive commandline cheatsheet tool
subtitle: You dont need to remember hundreds of commands from now.
description: Navi gives you freedom to search and store cheatsheet od commands you use.
image: https://devskrate.github.io/assets/blog-banners/navi.png
optimized_image: https://devskrate.github.io/assets/blog-banners/optimized/navi.webp
author: srisatyalokesh
category: [dev]
tags: [tips, developers, linux, mlogs]
---

Do you feel command-line is only for geeks or nerds?  
Do you feel hard to remember commands and it's options?  
Here is cheatsheet tool at your fingertips which will help you to browse through commands and make note of some new commands.  
You may come across many Linux tools but this will surely help for everyone who use Linux.

> There's nothing like NewBee(Noob) and Pro in Linux. It's an ocean of resources, Usage will completely depend on the work you do.

#### What is navi?

**Navi** is an interactive cheatsheet tool written in **Rust** for the **command-line and application launchers**. Just like Bro pages, Cheat, Tldr tools, Navi also provides a list of examples for a given command, skipping all other comprehensive text parts.

**Navi** allows you to browse through cheatsheets (that you may write yourself or download from maintainers) and execute commands, prompting for argument values.

from now you will never say any of these.

- How to run that command again?
- Oh, it's not in my bash history
- Damn, it's almost what I wanted but I need to change some args

See how cool navi is -
![navi-demo](https://devskrate.github.io/assets/images/mlogs/navi/navi-demo.gif)

#### Pros of navi

- it will make you type less;
- it will spare you from knowing CLIs by heart;
- it will teach you new one-liners.
- **Open Source tool**

It can be either used as a command or as a shell widget (Ctrl-R).
![navi-demo](https://devskrate.github.io/assets/images/mlogs/navi/navi-demo2.gif)

#### Installation

##### Using [Homebrew](http://brew.sh/) or [Linuxbrew](http://linuxbrew.sh/)

```batch
brew install navi
```

##### Using [cargo](https://github.com/rust-lang/cargo)

```batch
cargo install navi
```

##### Using install script

```batch
bash <(curl -sL https://raw.githubusercontent.com/denisidoro/navi/master/scripts/install)
```

##### Building from source

```batch
git clone https://github.com/denisidoro/navi ~/.navi
cd ~/.navi
make install
```

#### Usage

By running `navi` for the first time, you'll be suggested to download some _cheatsheets_. By running `navi` again, these _cheatsheets_ will appear.

#### Shell widget

You can use **navi** as a widget to your shell. This way, your history is correctly populated and you can edit the command as you wish before executing it. To set it up, add this line to your `.bashrc`-like file:

```sh
# bash
source <(navi widget bash)
```

Please refer to `navi --help` for more details or refer their [documentation](https://github.com/denisidoro/navi/blob/master/README.md)

Beauty of navi is you can see, understand and contribute to it as it is an **open source project**  
Here is the link for the repo on [GitHub](https://github.com/denisidoro/navi/)

##### Happy Quarantine

Please share your feedback on [twitter](https://twitter.com/devskrate), [Instagram](https://instagram.com/devskrate), or mail us at [support@devskrate.com](mailto:support@devskrate.com). Use [#DevsKrate](https://devskrate.com) on any social media platforms we will reach out to you.
