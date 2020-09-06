---
title: "Tmux: Shell khusus buat para hacker!"
date: 2020-08-30T06:13:32Z
lastmod: 2020-08-30T06:13:32Z
author: Zen
# authorlink: https://author.site
cover: /IMG_20200831_111026.jpg
tags:
  - linux
# showcase: true
draft: false
---

Kenyamanan adalah kunci dari programming.

<!--more-->

Sebagai programmer yang menghabiskan banyak waktunya di depan laptop, tentunya ingin merasakan kenyamanan saat programming, salah satunya adalah memilih _shell_ yang tepat.

Shell adalah interface dari Terminal. Biasanya kan kita menemukan bahwa yang termasuk shell adalah default shell, Fish, dan ZSH. Kalau Fish dan ZSH, biasanya untuk customisasi tampilan Terminal supaya enak dipandang. Nah, ada satu lagi nih shell yang memudahkan dan membuat kita nyaman dalam developing, yaitu Tmux.

Seperti ini tampilannya Tmux:

![Tampilan Tmux](/Screenshot_2020-09-05_11-58-40.png)

Keunggulan Tmux yang tampak dari screenshot di atas adalah layarnya yang bisa dibagi-bagi. Tentu ini berbeda dengan shell lainnya yang hanya mementingkan tampilan. Kalau Tmux, kelebihannya adalah layarnya yang bisa dibagi-bagi. Dan kurasa memang itu aja sih fiturnya. Hehehe...

Gimana? Lebih nyaman kan developingnya? Soalnya kan semua jendela Terminal terbuka sehingga kita nggak perlu lagi membuka tab Terminal satu per satu.

## Menginstall Tmux

Untuk menginstall Tmux, buka Terminalmu lalu ketikkan kode berikut:

```bash
sudo apt install tmux
```

## Menjadikan Tmux sebagai default shell

Untuk menjadikan Tmux sebagai default shell, buka dulu `~/.bashrc` lalu tambahkan kode berikut ini di awal dari kode-kode lainnya:

```bash
[[ $TERM != "screen" ]] && exec tmux
```

## Membagi layar Tmux

Ini adalah fitur utama dari Tmux yaitu membagi layar. Nah, berikut ini adalah kombinasi tombol untuk membagi layar:

| Membagi jadi | Tombol |
|---|---|
| kiri-kanan | `Ctrl` `b` `%` |
| atas-bawah | `Ctrl` `b` `"` |

## Berpindah cursor antarlayar Tmux

Untuk berpindah cursor aktif antarlayar Tmux, tekan `Ctrl` `b` lalu tekan mau berpindah ke arah mana. Contohnya aja seperti tabel di bawah ini:

| Arah | Tekan |
|---|---|
| Atas | `Ctrl` `b` `atas` |
| Kanan | `Ctrl` `b` `kanan` |
| Bawah | `Ctrl` `b` `bawah` |
| Kiri | `Ctrl` `b` `kiri` |

## Cara scroll di Tmux

Kalau di Terminal biasa kan, kalau mau scroll, kita tinggal gunakan scroll di mouse atau di touchpad buat scroll atas dan bawah. Tapi, kalau di Tmux, kalau kita scroll atas maupun bawah, yang tampil malah perintah sebelum dan sesudahnya, alias disamakan dengan kita memencet tombol atas dan bawah. Nah, kalau mau scroll, tekan dulu tombol `Ctrl` `b` `[` lalu kamu scroll.

Kalau sudah selesai scrollnya, mau masuk mode mengetik lagi, tekan aja `Esc`.