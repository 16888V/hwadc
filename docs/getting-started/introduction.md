---
layout: docs
title: Introduction
description: Bootsblogger adalah sebuah template dasar, untuk membangun template Blogger menggunakan Bootstrap, yang dirancang untuk memberikan kemudahan dan keindahan.
group: getting-started
redirect_from: "/getting-started/"
toc: true
---

Template dasar Bootsblogger sangat fleksibel, mudah dipahami, penulisan kode yang baik, terstruktur, dan menyediakan banyak fitur. Dengan itu semua, Anda dapat dengan mudah membangun template sesuai dengan yang Anda inginkan.

## Quick start

Anda dapat menggunakan Bootsblogger dengan dua cara, yaitu:

### Compiled template

Membangun template langsung di editor HTML Blogger, atau Anda dapat menggunakan *text editor* favorit Anda.

<a href="{{ site.download.dist }}" class="btn btn-bd">Download compiled template</a>

**Content:**

Hanya berisi template terkompilasi.

{% highlight plaintext %}
bootsblogger/
└── template.xml
{% endhighlight %}

Pasang `template.xml` di blog Anda, kemudian ubahsuaikan. Atau, ubahsuaikan menggunakan *text editor* favorit Anda, kemudian pasang template di blog Anda.

### Source files

Membangun template menggunakan [build tools]({{ site.baseurl }}/getting-started/build-tools/) dan *text editor* favorit Anda.

<a href="{{ site.download.source }}" class="btn btn-bd">Download source files</a>

**Content:**

Template terkompilasi, beserta kode sumber CSS, template, dan dokumentasi. Untuk lebih jelas lihat struktur di bawah ini.

{% highlight plaintext %}
bootsblogger/
├── dist/
│   └── template.xml
├── docs/
├── scss/
│   ├── bootsblogger/
│   └── bootstrap/
└── template-src/
    ├── default-markups/
    ├── includable/
    ├── partials/
    ├── post/
    ├── widgets/
    ├── config.json
    ├── index.xml
    ├── layout-mode.css
    ├── script.js
    └── skin.css
{% endhighlight %}

Ubahsuaikan semua kode sumber, kemudian [kompilasi]({{ site.baseurl }}/getting-started/build-tools/), dan pasang `dist/template.xml` di blog Anda.

- **`dist/template.xml`** - Template terkompilasi.
- **`docs/`** - Berkas-berkas dokumentasi.
- **`scss/`** - Kode sumber CSS Bootstrap dan Bootsblogger yang akan dikompilasi ke dalam `template-src/includable/assets/css`.
- **`template-src/index.xml`** - Untuk menyertakan keseluruhan bagian-bagian template, dan akan dikompilasi ke dalam `/dist`.

## Bootstrap

Untuk dapat membuat template yang super keren, Anda harus menguasai Bootstrap atau minimal mengetahui dasarnya. Untuk mempelajarinya silakan kunjungi halaman dokumentasi Bootstrap di <https://getbootstrap.com/>.
