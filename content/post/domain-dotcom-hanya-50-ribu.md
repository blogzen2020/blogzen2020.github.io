---
title: Ssst... Domain .com cuma 50 ribu loh!
date: 2020-08-31T21:25:22Z
lastmod: 2020-08-31T21:25:22Z
author: Zen
# authorlink: https://author.site
cover: /arnel-hasanovic-MNd-Rka1o0Q-unsplash.jpg
tags:
  - blogspot
# showcase: true
draft: false
---

Memiliki domain .com sudah menjadi kebutuhan bagi para blogger. Kok bisa?

<!--more-->

Tentu karena dengan memiliki domain .com, akan dengan sangat mudah menerima berbagai tawaran ala-ala blogger seperti content placement, product review, book review, link placement, dll.

Ya, nggak mesti .com sih. Intinya ya domain-domain TLD (top level domain) akan lebih mudah menerima tawaran kerja sama ala-ala blogger tadi. Katanya sih, daftar di Google Adsense juga lebih mudah kalau domainnya itu TLD.

Lalu, berapa sih harga domain .com itu? Berikut adalah harganya di beberapa perusahaan layanan hosting:

![Dotcom di Domainesia](/IMG_20200901_103803.jpg)

Kalau di Domainesia, 129 ribu per tahun.

![Dotcom di idcloudhost](/IMG_20200901_104433.jpg)

Di idcloudhost, 125 ribu per tahun.

![Domain di Niagahoster](/IMG_20200901_105101.jpg)

Kalau di Niagahoster, 125 ribu.

![Dotcom di idwebhost](/IMG_20200901_105410.jpg)

Di idwebhost, 129 ribu.

Jadi, rata-rata .com itu harganya sekitar **125 ribu sampai 129 ribu.**

## Mendapatkan domain .com 50 ribu

Jadi, kisahnya tu aku dapat broadcast di grup WA Ruang 2 Diskusi Web Programming yang isinya seperti ini:

```
OPEN DOMAIN TLD
( com / net / org / biz )

- Full Control Cloudflare
- Bebas Request Domain
- Masa Aktif 1 Tahun
- Bergaransi
- Legal 100%
- Cocok Buat Blog / Web Pribadi / Web P
Harga 40.000 / Domain

wa 1 : http://wa.me/6285758110924

wa 2 : http://wa.me/6281959679197
```

Kemudian, aku bertanya kepada kontak yang tersedia tentang mekanisme .comnya. Akhirnya, aku dapat penjelasan bahwasanya nanti domain yang kita sewa itu setting DNSnya menggunakan Cloudflare. Nah, apa itu Cloudflare? Daripada bingung, kita lanjut aja bacanya.

Jadi, pertama kamu tentukan dulu mau domain apa. Pakai domain yang belum dimiliki tentunya ya. Hehehehe. Misalnya aja _maumakanapa.com_. Lalu, chat ke kontak yang tersedia di broadcast yang aku lampirkan di atas yaitu [085758110924](https://wa.me/6285758110924) atau [081959679197](https://wa.me/6281959679197). Nah, nanti, kamu akan diminta bayar 40 ribu untuk tahun pertama. Nanti untuk tahun-tahun setelahnya, bayarnya 50 ribu. Murah kan jika dibandingkan dengan perusahaan hosting lainnya?

Kemudian, setelah transfer, dia akan minta emailmu untuk daftar Cloudflare. Lalu, dia akan minta kita untuk nunggu beberapa saat karena akun Cloudflarenya lagi diproses.

Terus, nanti kalau akun Cloudflarenya udah jadi, kita dikasih tau. Habis tu, kamu cek emailnya karena Cloudflare mengirim link verifikasi akun. Nah, kamu klik aja tu linknya. Maka, akun Cloudflare dan domain .commu sudah jadi. Selamat...

## Sambungkan Blogspot ke .com

Pertama, buka dulu dashboard Blogger lalu menuju ke bagian `Setelan`.

![Dashboard Blogger](/IMG_20200901_172437.jpg)

![Bagian setting Blogger](/IMG_20200901_172501.jpg)

Kemudian klik `Domain kustom`. Maka akan muncul:

![Dialog masukkan custom domain](/IMG_20200901_215402.jpg)

Nah, di bagian inputan itu kamu isi dengan nama domain yang **sudah** kamu pesan. Kalau di contoh itu, aku sudah memesan `www.hellohello2020.com` (**jangan lupakan `www`**).

Klik `SIMPAN`.

![Error saat pasang custom domain](/IMG_20200901_215834.jpg)

Maka, akan muncul pesan error. Nah, di pesan error ini, kita ambil beberapa hal penting aja yaitu:

| Nama | Tujuan |
|---|---|
| www | ghs.google.com |
| x664ampdtepe | gv-livnrnrfonsgai.dv.googlehosted.com |

Nah, empat teks itu jangan lupa dicatat ya. Bisa dicatat di WA atau di notes HP.

Kemudian, kita buka [dashboard Cloudflarenya](https://dash.cloudflare.com).

![Dashboard Cloudflare](/IMG_20200901_220612.jpg)

Klik nama domain yang udah kamu pesan tadi (di sini, aku berarti ngeklik `duniazen.com`).

> Anggap aja `duniazen.com` itu `hellohello2020.com`. Hehhehehe...

![Overview Cloudflare](/IMG_20200901_220929.jpg)

Klik `DNS`.

![Tambah record DNS](/IMG_20200901_222009.jpg)

Klik `Add record`.

Lalu, masukkan teks seperti di bawah ini:

![Mulai isi record DNS](/IMG_20200901_222214.jpg)

Yang perlu diperhatikan adalah _pastikan awannya yang berada di atas tombol Save itu **berwarna abu-abu**. Kalau belum, klik aja awannya_.

Kemudian, isi record berikutnya:

![Record kedua](/IMG_20200901_222545.jpg)

Darimana huruf-huruf itu? Nah, coba cek lagi error yang diberikan oleh Blogger tadi:

| Nama | Tujuan |
|---|---|
| www | ghs.google.com |
| x664ampdtepe | gv-livnrnrfonsgai.dv.googlehosted.com |

Nah, kita ambilnya dari situ.

Kemudian, masukkan juga:

![A record pertama](/IMG_20200901_223028.jpg)

![A record kedua](/IMG_20200901_223050.jpg)

![A record ketiga](/IMG_20200901_223105.jpg)

![A record keempat](/IMG_20200901_223115.jpg)

Kalau sudah, kembali ke Setelan Blogger lalu masukkan lagi kustom domainnya:

![Dialog masukkan custom domain](/IMG_20200901_215402.jpg)

Lalu klik `SIMPAN`.

Sudah selesai? Ya sudah sih.

> Tapi, kalau ada error, coba dihapus dulu kode-kodenya baru diisi lagi.

Jangan lupa juga buat setting `situs.com` diredirect ke `www.situs.com` dan diaktifin HTTPSnya:

![Finishing](/IMG_20200901_224313.jpg)

> Itu nama blognya anggap aja `hellohello2020.com` ya. Hehhehe...

## Atribusi

<https://unsplash.com/photos/MNd-Rka1o0Q?utm_source=unsplash&utm_medium=referral&utm_content=creditShareLink>