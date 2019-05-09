---
layout: docs
title: Default markups
description: Mengubahsuaikan gadget.
group: core-template
toc: true
---

Bootsblogger mengubahsuaikan gadget dengan menggunakan tag `b:defaultmarkups` dan `b:defaultmarkup`, tag ini dapat digunakan untuk membuat model gadget standar dalam template yang Anda buat.

## Usage

{% highlight html %}
<b:defaultmarkups>
  <b:defaultmarkup type='WIDGET_TYPE'>
    ...
  </b:defaultmarkup>
</b:defaultmarkups>
{% endhighlight %}

- Tag `b:defaultmarkups` sebaiknya diletakkan sebelum `</head>` atau `</body>`.
- Tag `b:defaultmarkups` hanya dapat berisi tag `b:defaultmarkup`.
- Tag `b:defaultmarkup` hanya dapat berisi tag `b:includable`.

Lihat `template-src/default-markups` untuk mempelajarinya.

## Customized gadgets

<table class="table table-bordered table-striped table-responsive">
  <thead>
    <tr>
      <th>Name</th>
      <th>Type</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Blog Archive</td>
      <td><code>BlogArchive</code></td>
    </tr>
    <tr>
      <td>Blog Search</td>
      <td><code>BlogSearch</code></td>
    </tr>
    <tr>
      <td>Contact Form</td>
      <td><code>ContactForm</code></td>
    </tr>
    <tr>
      <td>Featured Post</td>
      <td><code>FeaturedPost</code></td>
    </tr>
    <tr>
      <td>Follow by Email</td>
      <td><code>FollowByEmail</code></td>
    </tr>
    <tr>
      <td>Page Header</td>
      <td><code>Header</code></td>
    </tr>
    <tr>
      <td>Image</td>
      <td><code>Image</code></td>
    </tr>
    <tr>
      <td>Labels</td>
      <td><code>Label</code></td>
    </tr>
    <tr>
      <td>Popular Posts</td>
      <td><code>PopularPosts</code></td>
    </tr>
    <tr>
      <td>Translate</td>
      <td><code>Translate</code></td>
    </tr>
  </tbody>
</table>
