---
title: "Micro: Nulis buku dengan Terminal!"
date: 2020-09-11T00:24:33Z
lastmod: 2020-09-11T00:24:33Z
author: Zen
cover: /IMG_20200911_085735.jpg
tags:
  - linux
draft: true
---

Nggak cuma Word yang bisa dipakai ngetik...

<!--more-->

Yang menjadi kendala untuk mengetik di Terminal adalah karena nggak terbiasa. Misalnya aja Vim. Untuk keluar dari Vim, perintahnya itu `:wq`. Kan nggak biasa. Udah gitu juga, untuk berganti antara mode nulis dan mode scroll juga ada keyboard shortcutnya sendiri.

![Jokes Vim](/BgxWBRxjvNhnbM9DiyHtCptYaDNF3xx85r8if8spuMjfmZn5JXvqcsPohH4878fNXPfVCfqSxhRvwnT4GrsVFKSKeXbSssSPRQfULmyWfYjtoS4UHcaXn2pJb1eAppS2eFWDgo8tooi4EQqcDqsoDJqpAjeJQVz16eyQ4dyMEi5aHyp.jpeg)

## Kisah awal bagaimana aku menemukan Micro

## Menginstall Micro

Untuk Android (Termux), untuk penginstalannya tinggal mengetikkan perintah:

```bash
pkg install micro
```

Sedangkan kalau untuk Linux:

```bash
curl https://getmic.ro | bash
```

## Berbagai fitur di Micro

### Mengaktifkan softwrap

Tekan `Ctrl` `e`.

Ketikkan `set softwrap on` lalu enter.

### Mengaktifkan skema warna simpel

Tekan `Ctrl` `e`.

Ketikkan `set colorscheme simple` lalu enter.

### Membuka file

Contohnya aja, kita mau membuka file `makan-enak.md`, maka, perintahnya adalah:

```bash
micro makan-enak.md
```

### Menyimpan file

Tekan `Ctrl` `s`.

### Menutup file

Tekan `Ctrl` `q`.

## Atribusi

<https://steemit.com/meme/@bigdeej/linux-jokes-vim-meme>
