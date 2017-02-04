---
layout: docs
title: Labels - lists
description: Menampilkan daftar label dari data JSON menggunakan `<ul>`.
group: blogger-json-feeds
---

Menampilkan daftar label dari data JSON menggunakan `<ul>`.

## Config

Nama fungsi: `labelsLists`.

{% highlight html %}
<script>
var config = {
  postsPerPage: 10,
  badge: true|false,
  classes: {
    ul: 'Add class to ul',
    li: 'Add class to li',
    a: 'Add class to a',
    badge: 'badge badge-default badge-pill'
  }
}
</script>
{% endhighlight %}

**Catatan:** jika `badge: true`, dan Anda mempunyai banyak label, kecepatan memuat halaman mungkin akan berkurang.

## Example

{% example html %}
<script>
var config = {
  postsPerPage: 10,
  badge: true,
  classes: {
    ul: 'nav flex-column',
    li: 'nav-item',
    a: 'nav-link',
    badge: 'badge badge-default badge-pill'
  }
}
</script>
<script src="https://blogger.googleblog.com/feeds/posts/summary?max-results=0&amp;alt=json-in-script&amp;callback=labelsLists"></script>
{% endexample %}
