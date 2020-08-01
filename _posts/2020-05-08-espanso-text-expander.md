---
date: 2020-05-08 17:26:40
layout: post
title: Espanso - Cross-platform Text Expander written in Rust
subtitle: The best cross platform text expander available as of now
description: Espanso helps you to auto fil your details with ease
image: https://devskrate.github.io/assets/blog-banners/espanso.jpg
optimized_image: https://devskrate.github.io/assets/blog-banners/optimized/espanso.webp
category: [howto]
tags: [espanso, cross-platform, text expander]
author: nikhil
paginate: false
is_generated: false
---

Snippet tools are incredibly useful. The idea is to save time that would have otherwise been wasted typing phrases, sentences or entire paragraphs.

Espanso is an open source text template program for Windows, Mac and Linux that helps users save time.

During the installation, you have the choice to add Espanso to "PATH" (Windows System Variable) and to enable it to auto-start with Windows. You will also need to restart the computer to get the program working. properly; I think it requires the restart to enable the "PATH" correctly. Start the program and you should see an icon on the system tray. Right-clicking on it allows you to disable it or exit the program.

Espanso works in all applications including Notepad, Word, Firefox, Thunderbird, and more.

## Matches

Espanso uses the concept of Matches (keyword recognition) i.e., when you type a word that's present in the program's settings, it triggers the application to substitute the keyword with its configured replacement. The official wiki explains the technical details rather well, but I'll demonstrate how it works below for your convenience.

Fire up a text editor or browser, or any other program that accepts text input. Type the word :espanso and it will magically be replaced with the phrase "Hi there!". In this case ":espanso" is the keyword and "Hi There" is the replaced text.

![Espanso Demo](https://devskrate.github.io/assets/images/mlogs/espanso/espanso_feature.gif)

If you haven't guessed it already, Espanso is the Italian word for Expanded.

IndicateTLS highlights TLS security protocol version in Firefox's address bar
Capture images and annotate them quickly with Draft Notes
Capture images and annotate them quickly with Draft Notes

![Espanso Demo](https://devskrate.github.io/assets/images/mlogs/espanso/espanso-highlighted.jpeg)

So, how do we customize Espanso?
Go to the application's "Roaming" folder in your User directory.

This folder contains a "default.yml" file. Open it using a text editor, e.g. Notepad works just fine. Espanso uses YAML syntax, which is very user-friendly. Look at the highlighted section in the screenshot below. That's the match trigger and replacement which I mentioned in my example.

## Rules

The indentation is necessary for the syntax to work. So if your match isn't being triggered correctly, check the spacing in the syntax. The other rule is to remember to use the : symbol. For e.g. :espanso vs espanso. The first one is correct, the latter won't trigger the program.

## How to add new words to Espanso?

Let's try adding a new one. Write a new trigger word and choose a replacement phrase. To make it easy, you can just copy the "espanso" trigger, paste it in a new line and edit it.
Save the document, exit Espanso and start it again. Now type :ghx and it should be replaced with gHacks.net. That's incredibly easy, isn't it? You can use it to add email signatures, URLs, HTML Tags, commonly used phrases, responses, etc, and save some time.

![Espanso Demo](https://devskrate.github.io/assets/images/mlogs/espanso/espanso_yml.jpeg)

You can even replace a text with an image, the syntax is slightly different.

```yml
- trigger: ":word"
image_path: "/path/image.ext"
```

Replace word with the keyword you want and the /path/image.ext with the full path of the image's location, followed by the name of the picture and its extension. This may not be practical in day-to-day usage, but the option is there, in case you want to use it.

**Closing Words**:
Espanso is fast, easy to use if you want to quickly insert words and phrases.
