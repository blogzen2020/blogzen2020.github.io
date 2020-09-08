---
title: Virtual DOM tanpa framework
date: 2020-09-06T10:43:28Z
lastmod: 2020-09-06T10:43:28Z
author: Zen
cover: /img/avatar.jpg
tags:
  - dunia frontend
draft: true
---

Bisakah kita meninggalkan Vue, React, dan Angular?

<!--more-->

## Contoh dari _Virtual DOM_ tanpa framework

<table>
 <tbody>
  <tr>
   <td><button onclick="kurang()">&minus;</button></td>
   <td><div class="angka">0</div></td>
   <td><button onclick="tambah()">&plus;</button></td>
  </tr>
 </tbody>
</table>
<script>
 tambah = () => document.querySelector(".angka").innerText = Number(document.querySelector(".angka").innerText) + 1
 kurang = () => {
  if (document.querySelector(".angka").innerText > 0){
   document.querySelector(".angka").innerText = Number(document.querySelector(".angka").innerText - 1)
  }
 }
</script>

## Kodenya

```html
<table>
 <tbody>
  <tr>
   <td><button onclick="kurang()">&minus;</button></td>
   <td><div class="angka">0</div></td>
   <td><button onclick="tambah()">&plus;</button></td>
  </tr>
 </tbody>
</table>
<script>
 tambah = () => document.querySelector(".angka").innerText = Number(document.querySelector(".angka").innerText) + 1
 kurang = () => {
  if (document.querySelector(".angka").innerText > 0){
   document.querySelector(".angka").innerText = Number(document.querySelector(".angka").innerText - 1)
  }
 }
</script>
```