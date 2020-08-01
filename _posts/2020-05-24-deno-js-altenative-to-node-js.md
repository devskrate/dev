---
date: 2020-05-24 12:34:56
layout: post
title:  "What is Deno.js? How this competes with node.js?"
author: akash
category: [dev]
image: https://devskrate.github.io/assets/blog-banners/deno-js.jpg
optimized_image: https://devskrate.github.io/assets/blog-banners/optimized/deno-js.webp
tags: [developers, javascript, alternatives]
---

Deno is the creation of Ryan Dahl, which is a new JavaScript runtime for the backend, but instead of being written in C++, it’s written in Rust, based on the Tokio platform (which provides the asynchronous runtime needed by JavaScript), running on Google’s V8 engine. It is also a new runtime for executing JavaScript and TypeScript outside of the web browser. 


#### Why should we use this?   

Generally we may get a doubt, why should I use it, here are some of it's features. They are:

##### 1. Security is integrated

Node.js allows you to access read and write into the filesystem, access environment variables, make outgoing requests, etc. As well as it also opens up a security risk if you are not careful when writing code.

So instead, Deno uses command-line arguments to enable or disable access to different security features. So if you need your script to be able to access the /etc folder, you can do:
 
```sh
deno --allow-read=/etc myscript.ts
```
It will allow your code to read from the folder, anything else and you’ll get a security exception. This is similar to how other platforms handle security. 

##### 2. Complete standard library

Deno claims to have a complete standard library allowing developers to use official tools to perform basic tasks and only requiring the use of external libraries for complex tasks and it comes with the tools to add color to terminal text, generate UUIDs, work with external data structures,  and for writing WebSockets.

##### 3. Integrated Typescript

In Deno, by default the integration into JavaScript is done internally, so no need for external tooling. By default Deno takes care of a lot, you can overwrite the configuration by using your own tsconfig.json file:

```sh
deno run -c tsconfig.json [your-script.ts]
```
The default configuration of Deno is to use strict mode, so any ill-advised coding practice will be alerted immediately.


#### Deno Installation

Deno ships as a single executable with no dependencies. You can install it using the installers below: 

##### Using Shell (macOS, Linux):
```sh
$ curl -fsSL https://deno.land/x/install/install.sh | sh
```
##### Using PowerShell (Windows):
```sh
$ iwr https://deno.land/x/install/install.ps1 -useb | iex
```
##### Using Cargo (Windows, macOS, Linux):
```sh
$ cargo install deno
```
##### Using Homebrew (macOS):
```sh
$ brew install deno
```
##### Using Chocolatey (Windows):
```sh
$ choco install deno
```
##### Using Scoop (Windows):
```sh
$ scoop install deno
```


#### Where to learn Deno?

https://www.freecodecamp.org/news/the-deno-handbook/

