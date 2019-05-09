---
layout: docs
title: Build tools
description: Bootsblogger menggunakan Grunt untuk sistem pembuatan CSS, template, dan Jekyll untuk menulis dokumentasi.
group: getting-started
toc: true
---

Gruntfile Bootsblogger (`bootsblogger/Gruntfile.js`) menyediakan berbagai perintah Grunt untuk memberikan kemudahan dalam bekerja dengan Bootsblogger, seperti untuk kompilasi kode, menjalankan pengujian, dan lainnya.

## Tooling setup

Untuk dapat menggunakan *build system* Bootsblogger dan menjalankan dokumentasi secara lokal, Anda membutuhkan kode sumber Bootsblogger, Node, dan Grunt. Ikuti langkah-langkah di bawah ini:

1. [Unduh dan pasang Node](https://nodejs.org/download), yang digunakan untuk manajemen dependensi.
2. Pasang *Grunt command line tools*, `grunt-cli`, dengan `npm install -g grunt-cli`.
3. Pindah ke direktori *root* `/bootsblogger` dan jalankan perintah `npm install` untuk instalasi dependensi yang sudah terdaftar di dalam berkas `bootsblogger/package.json`.
4. [Pasang Ruby](https://www.ruby-lang.org/en/documentation/installation/), pasang [Bundler](https://bundler.io/) dengan `gem install bundler`, dan terakhir jalankan perintah `bundle install`. Ini akan memasang semua dependensi Ruby, seperti Jekyll dan *plugins*.
  - **Pengguna Windows:** Baca [panduan tidak resmi ini](http://jekyll-windows.juthilo.com/) agar Jekyll berjalan lancar tanpa masalah.

Setelah selesai, Anda dapat menjalankan berbagai perintah Grunt yang disediakan dari *command line*.

## Using Grunt

Gruntfile Bootsblogger meliputi *commands* dan *tasks* berikut:

| Task | Description |
| --- | --- |
| `grunt` | Jalankan perintah `grunt` untuk menjalankan pengujian dan kompilasi CSS dan template. |
| `grunt test` | Jalankan perintah `grunt test` jika Anda hanya ingin menjalankan pengujian. |
| `grunt watch` | Ini adalah metode paling nyaman untuk memonitor perubahan pada berkas Sass dan template, dan secara otomatis akan melakukan pengujian dan kompilasi setiap kali Anda menyimpannya. |

## Local documentation

Menjalankan dokumentasi secara lokal membutuhkan penggunaan Jekyll. Berikut adalah cara untuk memulainya:

1. Pastikan sudah menyelesaikan [*tooling setup*](#tooling-setup) di atas untuk instalasi Jekyll (*the site builder*) dan dependensi Ruby lainnya dengan `bundle install`.
2. Dari direktori *root* `/bootsblogger`, jalankan perintah `bundle exec jekyll serve`.
3. Buka <http://localhost:9002> di *browser* Anda, selesai.

Pelajari lebih lanjut tentang penggunaan Jekyll dengan membaca [dokumentasinya](https://jekyllrb.com/docs/home/).

## Troubleshooting

Jika Anda mendapat masalah ketika instalasi, hapus direktori `node_modules` dan jalankan kembali perintah `npm install`.
