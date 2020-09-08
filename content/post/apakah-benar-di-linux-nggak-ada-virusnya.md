---
title: Kok bisa ya Linux nggak ada virusnya?
date: 2020-09-08T04:50:38Z
lastmod: 2020-09-08T04:50:38Z
author: Zen
cover: /IMG_20200908_192533.jpg
tags:
  - linux
draft: false
---

OTW Linux lah.

<!--more-->

Virus adalah sebuah program komputer yang digunakan untuk merusak targetnya. Metode pengrusakannya pun beraneka macam. Ada virus yang hanya menyisipkan iklan di komputer korban, disebut dengan virus Ads. Ada virus yang menghubungkan jaringan target ke komputer hacker, virus ini bernama Trojan. Ada pula virus yang membuat semua folder dan file menjadi shortcut. Nama virusnya adalah Worm. Hingga yang paling menjadi mimpi buruk akhir-akhir ini: Ransomware!

Lalu, yang menjadi pertanyaan adalah **Apakah virus hanya menyerang sistem operasi Windows?** Lalu, bagaimana dengan Linux? Apakah Linux nggak ada virusnya?

Kalau dilihat dari definisi di atas bahwasanya virus hanyalah _sebuah program komputer_, maka tentu saja Linux juga bisa terserang virus. Tapi, kenapa kok seolah-olah bahwa virus hanya menyerang Windows?

Ada dua alasan dibalik _amannya_ Linux dari berbagai virus. Yang pertama adalah pengguna yang lebih sedikit dibandingkan Windows. Lalu yang kedua adalah proteksi rootnya.

Kalau dari alasan pertama sudah pasti lah bahwa kita sejak SMP diajarkan menggunakan Windows, bukan Linux maupun Mac. Maka, kita pun akhirnya sudah terbiasa dengan Windows. Padahal, dari segi tampilan, saat ini Windows sama Linux sudah mirip. Bahkan, untuk office aja sudah ada WPS yang cara menggunakannya pun sama saja dengan Windows. Lalu, mengapa masih lebih banyak pengguna Windows daripada Linux?

Kemudian, alasan kedua adalah proteksi root. Kalau di Linux, password user komputer itu wajib karena untuk mengakses root diperlukan password itu. Makanya, ketika kita menginstall Linux, nggak bisa mengosongkan password komputer. Pasti harus diisi. Nah, kemudian, untuk mengakses root itu nggak bisa secara otomatis. Harus secara manual.

Gampangnya aja, misal kita ingin menginstall WPS di Linux menggunakan Terminal, maka kita harus mengetikkan kode:

```bash
sudo apt install wps-office
```

Aslinya kan, perintah penginstalannya itu hanya dimulai dari `apt`. Lalu, apakah itu `sudo`?

Sudo adalah kode yang digunakan untuk mengakses root. Pengaksesan root di sini adalah karena kita perlu memodifikasi root untuk menginstall aplikasi.