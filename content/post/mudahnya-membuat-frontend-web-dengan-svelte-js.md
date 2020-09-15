---
title: Mudahnya Membuat Frontend Web dengan Svelte JS
date: 2020-09-15T19:26:25+08:00
lastmod: 2020-09-15T19:26:25+08:00
author: Zen
cover: /img/avatar.jpg
tags:
  - psikologi
draft: true
---

Write less, do more!

<!--more-->

Sekarang adalah zamannya serba framework Javascript! Dimulai dari React, Vue, dan Angular, lalu ada pula yang namanya Svelte, sebuah framework Javascript yang sangat jarang disebutkan namanya. Mengapa sih jarang disebutkan? Entah. Tapi memang kita sudah terbiasa ketika menyebutkan tentang framework Javascript ya hanya sebatas React, Vue, dan Angular. Mungkin bisa dibilan karena Svelte ini termasuk baru, makanya jarang disebutkan.

Svelte JS dibuat oleh Rich Harris, seorang desainer di New York Times, pada tahun 2016. Svelte membuat gebrakan baru di dunia framework dengan suatu pertanyaan sederhana:

> Bisa nggak sih kita membuat sebuah compiler Javascript tapi dengan pengalaman developer yang bagus?

Akhirnya jadilah Svelte!

Kalau misalnya framework Javascript lainnya kan dia itu memuat kode frameworknya dulu baru setelah itu memuat kode yang kita buat. Kalau Svelte ini, dia langsung memuat kode yang kita buat yang telah dicompile oleh Svelte. Jadinya, kode yang jadi akan lebih kecil sizenya jika dibandingkan dengan hasil olahan dari framework lainnya.

Kodenya pun sangat mudah. Misalnya aja untuk membuat Hello World tapi dengan reactive, kodenya hanya seperti ini:

```html
<p>Hello {nama}!</p>

<script>
	let nama = 'World'
</script>
```

Simpel banget kan ya!

Coba deh kita bandingkan dengan Vue yang CDN, untuk membuat Hello World aja, kodenya perlu sepanjang ini:

```html
<div class="vue">
	<p>Hello {{ nama }}!</p>
</div>

<script type="text/javascript">
	new Vue({
		el: '.vue',
		data: {
			nama: 'World'
		}
	})
</script>
```

Kemudian, kalau untuk membuat input output yang reactive, kodenya seperti ini:

```html
<input type="text" bind:value='nama' name="">
<p>{nama}</p>

<script type="text/javascript">
	let nama = ''
</script>
```

Maka, otomatis saat mengisi teks input itu, akan tercetak di bawahnya hasilnya.

## Install Svelte

Untuk menginstall Svelte, pastikan kamu memiliki Node JS versi 10 ke atas. Lalu, ketikkan perintah berikut di Terminal:

```bash
npx degit sveltejs/template nama-projectnya
```

Kemudian, masuk ke `nama-projectnya` baru setelah itu ketikkan `npm i`.