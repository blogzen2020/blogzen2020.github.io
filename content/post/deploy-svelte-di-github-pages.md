---
title: Deploy Svelte Di Github Pages
date: 2020-09-13T08:09:49Z
lastmod: 2020-09-13T08:09:49Z
author: Zen
cover: /img/avatar.jpg
tags:
  - dunia frontend
draft: true
---

Cut out summary from your post content here.

<!--more-->

Buat file `.github/workflows/build.yml`:

```yml
name: build svelte

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

      - name: Setup Node
        uses: actions/setup-node@v1
        with:
          node-version: "14.x"
          
      - name: Cache dependencies
        uses: actions/cache@v1
        with:
          path: ~/.npm
          key: ${{ runner.os }}-node-${{ hashFiles('**/package-lock.json') }}
          restore-keys: ${{ runner.os }}-node-

      - name: Install
        run: npm i

      - name: Build
        run: npm run build

      - name: Deploy
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./public
```