---
title: Cara mudah membuat daftar isi di Hugo
date: 2020-09-03T19:27:49Z
lastmod: 2020-09-03T19:27:49Z
author: Zen
# authorlink: https://author.site
cover: /patrick-tomasso-Oaqk7qqNh_c-unsplash.jpg
tags:
  - dunia frontend
# showcase: true
draft: false
---

Membuat daftar isi di Hugo lebih mudah daripada di Blogger.

<!--more-->

Kalau di Blogger, untuk membuat daftar isi di sebuah postingan harus dilakukan secara manual dengan menuliskan list yang berisi subjudul-subjudul di artikel tersebut.

Sedangkan, kalau di Hugo, kamu bisa melakukannya secara otomatis. Atau bisa dibilang bahwa kamu cukup mengetikkan kodenya sekali aja buat dipakai berkali-kali. Hemat kan ya?

## Kode daftar isi di Hugo

Pertama, buka dulu file `themes/nama-temanya/layouts/_default/single.html`. Nah perhatikan pada `nama-temanya`. Itu, bisa macem-macem ya namanya. Tergantung yang buat tema Hugonya.

Setelah membuka filenya, coba cari kode `.Content`. Nah, `.Content` itu adalah isi dari postingan. Kalau di tema Hugo yang aku gunakan, untuk bagian isi postingan, kodenya adalah:

```html
<article style="margin-top: 2rem;">
 {{ .Content | emojify }}
</article>
```

Lalu, di atasnya `.Content`, masukkan kode berikut:

```html
<h2>Daftar isi</h2>
{{ .TableOfContents }}
```

Sehingga, untuk kode Hugo di blogku menjadi:

```html
<article style="margin-top: 2rem;">
 <h2>Daftar isi</h2>
 {{ .TableOfContents }}
 {{ .Content | emojify }}
</article>
```

## Menyembunyikan subjudul Daftar Isi jika nggak ada daftar isinya

Kalau berdasarkan kode di atas, subjudul `Daftar isi` akan selalu ada walaupun nggak ada daftar isinya. Jadinya kan malah aneh. Ada subjudul Daftar isi tapi nggak ada daftar isinya. Nah, akan kita sembunyikan.

Kalau kode di atas kan:

```html
<article style="margin-top: 2rem;">
 <h2>Daftar isi</h2>
 {{ .TableOfContents }}
 {{ .Content | emojify }}
</article>
```

Sekarang, untuk subjudul Daftar isi, kasih class `daftar-isi`:

```html
<article style="margin-top: 2rem;">
 <h2 class="daftar-isi">Daftar isi</h2>
 {{ .TableOfContents }}
 {{ .Content | emojify }}
</article>
```

Kemudian, masukkan kode Javascript ini di bawahnya:

```html
<script>
 if (document.querySelector("#TableOfContents").innerText.length == 0){
  document.querySelector(".daftar-isi").style.display = "none"
 }
</script>
```

Sehingga, kodenya menjadi:

```html
<article style="margin-top: 2rem;">
 <h2 class="daftar-isi">Daftar isi</h2>
 {{ .TableOfContents }}
 {{ .Content | emojify }}
</article>
<script>
 if (document.querySelector("#TableOfContents").innerText.length == 0){
  document.querySelector(".daftar-isi").style.display = "none"
 }
</script>
```

## Atribusi

<https://unsplash.com/photos/Oaqk7qqNh_c?utm_source=unsplash&utm_medium=referral&utm_content=creditShareLink>