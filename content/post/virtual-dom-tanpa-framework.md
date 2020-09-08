---
title: Virtual DOM tanpa framework
date: 2020-09-08T18:07:10Z
lastmod: 2020-09-08T18:07:10Z
author: Zen
cover: /Screenshot_2020-09-08_22-43-36.png
tags:
  - dunia frontend
draft: false
---

Bisakah kita meninggalkan Vue, React, dan Angular?

<!--more-->

React sebagai library Javascript buatan Facebook hadir dengan konsep virtual DOM di mana data dari DOM di HTML diolah oleh Javascript. Lalu, diikuti oleh framework Javascript lainnya yaitu Vue dan Angular yang juga mengadopsi virtual DOM dengan teknik yang berbeda. Kalau React itu full Javascript, artinya HTML dan CSS juga dimasukkan ke dalam Javascript, kalau Vue dan Angular, dipisah HTML, CSS, dan Javascriptnya.

Virtual DOM membuat kita lebih mudah dalam membuat dan memantainance suatu aplikasi. Namun, kelemahan dari virtual DOM adalah ukurannya yang besar sehingga muncul pertanyaan dari benak kita: Ada nggak sih caranya menerapkan teknik virtual DOM tanpa harus meload library/framework Javascript terlebih dahulu? Untuk saat ini, yang terpikir olehku adalah dengan menggunakan API `querySelector` dan `querySelectorAll`.

## Contoh dari _Virtual DOM_ tanpa framework

Seperti ini contoh dari penerapan virtual DOM tanpa meload library/framework Javascript:

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

Jadi, ketika kita memencet angka `tambah` maka akan bertambah angka yang ada di tengah dan jika memencet angka `kurang` maka akan berkurang angka yang ada di tengah.

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