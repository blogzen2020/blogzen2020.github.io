---
title: Cara super simpel untuk deploy Hugo di Github Pages
date: 2020-09-03T13:01:45Z
lastmod: 2020-09-03T13:01:45Z
author: Zen
# authorlink: https://author.site
cover: /thomas-jensen-QABDpFYhNpk-unsplash.jpg
tags:
  - dunia frontend
# showcase: true
draft: false
---

Dengan Hugo, kamu bisa membuat blog secara offline.

<!--more-->

Itu adalah salah satu fitur andalan Hugo. Masih banyak sih fitur lainnya. Jadi, Hugo ini semacam content management system (CMS) sebagaimana Blogger, Wordpress, Kompasiana, Jekyll, Gatsby, dll.

Namun, yang membedakan Hugo dari yang lainnya adalah karena dia sistemnya SSG (static site generator). Nah, sistem dari SSG ini adalah mengolah berbagai file Markdown menjadi sebuah blog sesuai dengan aturan yang telah ditetapkan oleh template.

Mungkin di postingan ini aku nggak akan membahas secara lebih mendalam tentang apa itu Hugo, bagaimana cara menggunakan Hugo, bagaimana cara memilih tema Hugo, dll. Karena memang postingan ini khusus untuk mendeploy atau mengolah Hugo menjadi blog di Github Pages.

Sebagaimana yang kita tau, Github Pages adalah layanan **gratis** dari Github untuk mengolah file-file Markdown menjadi sebuah blog menggunakan SSG Jekyll. Cuma Jekyll. Jadi, kalau kita ingin mendeploy Hugo di Github Pages, tentu caranya berbeda, nggak cuma upload aja ke Github.

Jadi, kita buat dulu Github Actionnya atau bisa dengan membuat file `.github/workflows/hugo.yml` yang isinya adalah:

```yaml
name: deploy hugo

on:
  push:
    branches:
      - master

jobs:
  deploy:
    runs-on: ubuntu-18.04
    steps:
      - uses: actions/checkout@v2
        with:
          submodules: true

      - name: Setup Hugo
        uses: peaceiris/actions-hugo@v2
        with:
          hugo-version: '0.74.3'
          # extended: true

      - name: Build
        run: hugo --minify

      - name: Deploy
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./public
```

Setelah membuat filenya, kamu tinggal mengolah blogmu yang berbasis Hugo itu lalu diupload ke Github. Maka, secara otomatis, file-file Hugomu itu akan berubah menjadi blog karena script di atas itu akan menjalankan Github Action yang akan mengolah file-file Hugo.

## Atribusi

<span>Photo by <a href="https://unsplash.com/@thomasjsn?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText">Thomas Jensen</a> on <a href="https://unsplash.com/s/photos/hugo?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText">Unsplash</a></span>