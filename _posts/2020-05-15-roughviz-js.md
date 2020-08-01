---
date: 2020-05-15 22:36:58
layout: post
title:  RoughViz.js - for creating sketchy/hand-drawn styled charts
subtitle: Let's make some cool and catcy sketches
description: Simple java script library to draw hand-drawn sketches
image: https://devskrate.github.io/assets/blog-banners/roughviz-js.jpg
optimized_image: https://devskrate.github.io/assets/blog-banners/optimized/roughviz-js.webp
author: srisatyalokesh
category: [dev]
tags: [developers, javascript, tutorials]
---

Visualization through visual imagery has been an effective way to communicate both abstract and concrete ideas since the dawn of humanity. Usually we do see some cool visualizations with great look and feel. But this is an out of box JavaScript Library which helps you to plot graphs as hand-drawn charts.

##### What is RoughViz.js?
**roughViz.js** is a reusable **JavaScript** library for creating sketchy/hand-drawn styled charts in the browser, based on [D3.js v5](https://d3js.org/), [roughjs](https://roughjs.com/), and [handy](http://handyjs.org/).

See some basic examples here - 
![roughviz](https://raw.githubusercontent.com/jwilber/random_data/master/roughViz.gif)

##### Why RoughViz.js?
Use these charts where the communication goal is to show intent or generality, and not absolute precision. Or just because they're fun and look weird. In our view those which will look weird will get more attention first than the best one. If you can create content which looks like hand-drawn images, sure you'll get appreciation.


##### Features

**Chart Types** (many more to come!)
<ul>
 <li>Bar (<code>roughViz.Bar</code>) <a href="#Bar">API</a>. <a href="https://blockbuilder.org/jwilber/4dc5235f7ea5e51ac1219b3605f5af6a">Example</a>.</li>
<li> Horizontal Bar (<code>roughViz.BarH</code>) <a href="#BarH">API</a>. <a href="https://blockbuilder.org/jwilber/419fa6d878fe6c0f79a28f9fc72d7ec6">Example</a>.</li>
<li> Donut (<code>roughViz.Donut</code>) <a href="#Donut">API</a>. <a href="https://blockbuilder.org/jwilber/e713c03097950d53a8cfde4c23aa292f">Example</a>.</li>
<li> Line (<code>roughViz.Line</code>) <a href="#Line">API</a>. <a href="https://blockbuilder.org/jwilber/ec7cbc374c2dc61b255494511e7d7ac6">Example</a>.</li>
<li> Pie (<code>roughViz.Pie</code>) <a href="#Pie">API</a>. <a href="https://blockbuilder.org/jwilber/d117e0b0864a161bec2d914013ed69da">Example</a>.</li>
<li> Scatter (<code>roughViz.Scatter</code>) <a href="#Scatter">API</a>. <a href="https://blockbuilder.org/jwilber/d02e4381d776fb9a7bcb126d3b32c85b">Example</a>.</li>
 <li> Stacked Bar (<code>roughViz.StackedBar</code>) <a href="#StackedBar">API</a>. <a href="https://blockbuilder.org/jwilber/ee35865631cb805057142568fa5fd090">Example</a>.</li>
 </ul>

Apply the features of `roughjs` to each chart:

- **roughness**
<img src="https://raw.githubusercontent.com/jwilber/random_data/master/roughViz_roughnessbars.webp"  alt="roughness examples">

- **fillStyle**
<img src="https://raw.githubusercontent.com/jwilber/random_data/master/rough_fillStyles.webp"  alt="fillStyle examples">


- **fillWeight**
<img src="https://raw.githubusercontent.com/jwilber/random_data/master/roughViz_fillweight.webp"  alt="fillStyle examples">


You'll get to know some more cool options in [API](https://github.com/jwilber/roughViz/blob/master/README.md#API) Documentation.

##### Installation

Via CDN (expose the `roughViz` global in `html`):

```html
<script src="https://unpkg.com/rough-viz@1.0.6"></script>
```

Via `npm`:

```
npm install rough-viz
```

Want to use with `React`? [There's a wrapper!](https://github.com/Chris927/react-roughviz):

```
npm install react-roughviz
```

Want to use with `Vue`? [There's a wrapper!](https://github.com/jolo-dev/vue-roughviz):

```
npm install vue-roughviz
```

Want to use it with `Python`? 
There are two options for this.

[Option 1](https://github.com/hannansatopay/roughviz) :
```
pip install roughviz
```
[Option 2](https://github.com/charlesdong1991/py-roughviz) :
```
pip install py-roughviz
```

##### How to Contribute?

This is an open-source project by four engineers. Source is on [GitHub](https://github.com/jwilber/roughViz/)


Share your most loved extensions and your feedback on [twitter](https://twitter.com/devskrate), [Instagram](https://instagram.com/devskrate), or mail us at [support@devskrate.com](mailto:support@devskrate.com). Use [#DevsKrate](https://devskrate.com) on any social media platforms we will reach out to you.
