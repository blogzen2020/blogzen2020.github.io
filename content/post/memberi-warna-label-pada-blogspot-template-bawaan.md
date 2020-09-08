---
title: Memberi warna label pada Blogspot template bawaan
date: 2020-09-06T05:16:27Z
lastmod: 2020-09-06T05:16:27Z
author: Zen
# authorlink: https://author.site
cover: /IMG_20200906_132429.jpg
tags:
  - literasi
# showcase: true
draft: false
---

Bisa loh memberi warna pastel untuk list label!

<!--more-->

## Before

![Sebelumnya](/IMG_20200906_132235.jpg)

## After

![Jadinya](/IMG_20200906_132429.jpg)

## Kodenya

Letakkan sebelum `</body>`:

```html
<script>
//<![CDATA[
warna = [
"rgb(244, 67, 54)",
"rgb(233, 30, 99)",
"rgb(156, 39, 176)",
"rgb(103, 58, 183)",
"rgb(63, 81, 181)",
"rgb(33, 150, 243)",
"rgb(3, 169, 244)",
"rgb(0, 188, 212)",
"rgb(0, 150, 136)",
"rgb(76, 175, 80)",
"rgb(139, 195, 74)",
"rgb(205, 220, 57)",
"rgb(255, 193, 7)",
"rgb(255, 152, 0)",
"rgb(255, 87, 34)",
"rgb(121, 85, 72)",
"rgb(158, 158, 158)",
"rgb(96, 125, 139)",
"rgb(0, 0, 0)"
]
warna.sort((a, b) => 0.5 - Math.random())
document.querySelectorAll(".post-labels a").forEach((x, n) => {
 x.style.background = warna[n]
 x.style.color = "white"
})
//]]>
</script>
```