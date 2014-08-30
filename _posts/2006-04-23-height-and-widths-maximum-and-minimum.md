---
title: Height and widths - maximum and minimum
author: Andrei
layout: post
permalink: /2006/04/height-and-widths-maximum-and-minimum/
categories:
  - Information Technology
  - Solution
tags:
  - designer
  - html
---
IE defines the "height" CSS property with a touch of flexibility. It means that the block should have at least the defined height.

In order to set a maximum height you need to set its "max-height" CSS property.

In Firefox, "height" means height! Meaning that your content will go outside the block, if it does not fit.

In order to set a minimum height you need to set its "min-height" CSS property and mask the "height", in order to let only IE see it (use "_height").