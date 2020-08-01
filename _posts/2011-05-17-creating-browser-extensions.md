---
date: 2020-07-01 17:26:40
layout: post
title: "Creating browser extensions"
subtitle: "Browser Extensions"
description: >-
  An easy way of creating a browser extension, with a hello world type extension.
image: >-
  https://devskrate.github.io/assets/blog-banners/files-secure-folder.jpg
optimized_image: >-
  https://devskrate.github.io/assets/blog-banners/optimized/files-secure-folder.webp
tags: [extensions, browser, script]
category: [dev]
author: puneeth
is_generated: true
---

Writing extensions is not that difficult, if you had an implementation with you and if you know basic web technologies like html, css and js, it is quiet enough for building a basic extension.

In this tutorial we will build a basic chrome extension that allows the user to change the background color of any page on `DevsKrate.com`.

Before getting started, know the basic things. When you click on an extension, we get a popup, it is a html file. We need to design the html page and the script behind it.

- Firstly create a directory with the name of your extension. Let us name our extension as "dev example".

#### Create the Manifest file

Every extension start from their manifest file, so create a `manifest.json` and include the following code.

```json
{
  "name": "dev example",
  "version": "1.0",
  "description": "First extension example!",
  "manifest_version": 2
}
```

The manifest file is the blueprint for the Extension. It tells the browser engine what version of the Extension API the Extension expects, the name and description of the Extension, and lots of other details.

1. Now open chrome and enter `chrome://extensions` in the url bar to open chrome extensions page or it can be opened by clicking on the Chrome menu, hovering over More Tools then selecting Extensions.
2. Enable Developer Mode by clicking the toggle switch next to Developer mode.
3. Click the LOAD UNPACKED button and select the extension directory.
   Ta-da! The extension has been successfully installed. Because no icons were included in the manifest, a generic toolbar icon will be created for the extension.

#### Add Instruction

Now the second step is to add the instructions(script) what our extension needs to do.
Before that we need to include the background script in the manifest file.

**Remember** Background scripts, and many other important components, must be registered in the `manifest`. Registering a background script in the manifest tells the extension which file to reference, and how that file should behave.

Update the manifest file with the below code:

```json
{
  "name": "dev example",
  "version": "1.0",
  "description": "First extension example!",
  "background": {
    "scripts": ["background.js"],
    "persistent": false
  },
  "manifest_version": 2
}
```

Now create `background.js` file and then include the below code. It sets the background color.

```js
chrome.runtime.onInstalled.addListener(function () {
  chrome.storage.sync.set({ color: "#3aa757" }, function () {
    console.log("The color is green.");
  });
});
```

- This script uses **storage API** for storing the color values. Including storage API and other API's we should give permission in the manifest file. So include the following code in the `manifest.json`.

```json
{
  "name": "dev example",
  "version": "1.0",
  "description": "First extension example!",
  "permissions": ["storage"],
  "background": {
    "scripts": ["background.js"],
    "persistent": false
  },
  "manifest_version": 2
}
```

#### Introduce a User Interface

Extensions can have many forms of a user interface, but this one will use a popup. Create a file named `popup.html` in the extension directory.

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      button {
        height: 30px;
        width: 30px;
        outline: none;
      }
    </style>
  </head>
  <body>
    <button id="changeColor"></button>
  </body>
</html>
```

- Now same as the `background.js` script, we should mention the `popup.html` in the manifest under `page_action`, like

```json
"page_action": {
      "default_popup": "popup.html"
},
```

- We should also include the icons for our extensions in the `manifest.json` file as

```json
"default_icon": {
        "16": "images/get_started16.webp",
        "32": "images/get_started32.webp",
        "48": "images/get_started48.webp",
        "128": "images/get_started128.webp"
      }
```

Download the images <a href="https://devskrate.github.io/assets/images/browser/chrome/chrome-extensions-images.zip" download="images">here</a>.

- There is also need of images for permissions warning, and favicon. These images are designated in the `manifest.json` under `icons`

```json
"icons": {
      "16": "images/get_started16.webp",
      "32": "images/get_started32.webp",
      "48": "images/get_started48.webp",
      "128": "images/get_started128.webp"
    },
```

- Add declared rules to the `background.js` script with the `declarativeContent API` within the `runtime.onInstalled` listener event.

```js
chrome.declarativeContent.onPageChanged.removeRules(undefined, function () {
  chrome.declarativeContent.onPageChanged.addRules([
    {
      conditions: [
        new chrome.declarativeContent.PageStateMatcher({
          pageUrl: { hostEquals: "developer.chrome.com" },
        }),
      ],
      actions: [new chrome.declarativeContent.ShowPageAction()],
    },
  ]);
});
```

- The extension will need permission to access the `declarativeContent` API in its `manifest.json`.

```json
{
  "name": "Getting Started Example",
...
  "permissions": ["declarativeContent", "storage"],
...
}
```

The browser will now show a full-color page action icon in the browser toolbar when users navigate to a URL that contains `DevsKrate.com`. When the icon is full-color, users can click it to view `popup.html`.

- The last step for the popup UI is adding color to the button. Create and add a file called `popup.js` with the following code to the extension directory.

```js
let changeColor = document.getElementById("changeColor");

chrome.storage.sync.get("color", function (data) {
  changeColor.style.backgroundColor = data.color;
  changeColor.setAttribute("value", data.color);
});
```

This code grabs the button from `popup.html` and requests the color value from storage. It then applies the color as the background of the button. Include a script to `popup.js` in `popup.html`.

```html
<script src="popup.js"></script>
```

#### Layer Logic

The extension now knows the popup should be only available to website `DevsKrate.com` and displays a colored button when the website is opened, but needs logic for further user interaction. Update `popup.js` and include the following code

```js
changeColor.onclick = function (element) {
  let color = element.target.value;
  chrome.tabs.query({ active: true, currentWindow: true }, function (tabs) {
    chrome.tabs.executeScript(tabs[0].id, {
      code: 'document.body.style.backgroundColor = "' + color + '";',
    });
  });
};
```

The updated code adds an onclick event the button. This turns the background color of the page the same color as the button.

- The `manifest.json` will need the `activeTab` permission to allow the extension temporary access to the tabs API. This enables the extension to call `tabs.executeScript`.

```json
"permissions": ["activeTab", "declarativeContent", "storage"]
```

The extension is now fully functional! Reload the extension, refresh this page, open the popup and click the button to turn it green! However, some users may want to change the background to a different color, so we need to provide options to the users.

#### Users Options

The extension currently only allows users to change the background to green. Including an options page gives users more control over the extension's functionality, further customizing their browsing experience.

- Create `options.html` and include the following code

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      button {
        height: 30px;
        width: 30px;
        outline: none;
        margin: 10px;
      }
    </style>
  </head>
  <body>
    <div id="buttonDiv"></div>
    <div>
      <p>Choose a different background color!</p>
    </div>
  </body>
  <script src="options.js"></script>
</html>
```

Then register this in the `manifest.json` page by adding this line, in the middle.

```json
"options_page": "options.html",
```

Now everything is fine, but if user goes the `options.html` page and selects the color, we need to change it, so we need a script for it.
Create a `options.js` file in the directory.

```js
let page = document.getElementById("buttonDiv");
const kButtonColors = ["#3aa757", "#e8453c", "#f9bb2d", "#4688f1"];
function constructOptions(kButtonColors) {
  for (let item of kButtonColors) {
    let button = document.createElement("button");
    button.style.backgroundColor = item;
    button.addEventListener("click", function () {
      chrome.storage.sync.set({ color: item }, function () {
        console.log("color is " + item);
      });
    });
    page.appendChild(button);
  }
}
constructOptions(kButtonColors);
```

Just refresh the extension!!, kudos you have built a basic extension.
Test by going to `DevsKrate.com`, it will work for all the pages of the Domain, check it out.

It will not work for the article(posts) pages because we have a dark theme for our articles, so you need to give special permissions to overwrite it and give the background color.
