---
layout: docs
title: Navmenu
description: Navmenu adalah komponen untuk membuat navigasi, dan dukungan elemen lainnya. Navmenu tampil secara vertikal.
group: components
toc: true
---

## How it works

Bungkus [konten](#supported-content) dengan `.navmenu`, dan tambahkan kelas [skema warna](#color-schemes).

## Color schemes

Tentukan skema warna navmenu dengan mengeset `background-color` dan `border-color`, Anda dapat menggunakan kelas utilitas warna atau membuat *custom styles*.

Gunakan `.navmenu-light` atau `.navmenu-dark` untuk menyesuaikan warna teks dengan warna latar belakang. `.navmenu-light` untuk latar belakang yang berwarna terang dan `.navmenu-dark` untuk latar belakang yang berwarna gelap.

<div class="bd-example">
  <nav class="navmenu navmenu-dark bg-dark mb-3">
    <a class="navmenu-brand" href="#">Bootsblogger</a>
    <div class="navmenu-nav">
      <a class="nav-item nav-link" href="#">Nav item</a>
      <a class="nav-item nav-link" href="#">Nav item again</a>
      <a class="nav-item nav-link" href="#">Another nav item</a>
    </div>
    <div class="navmenu-nav">
      <a class="nav-item nav-link active" href="#">Active</a>
      <a class="nav-item nav-link disabled" href="#">Disabled</a>
    </div>
  </nav>

  <nav class="navmenu navmenu-dark bg-primary mb-3">
    <a class="navmenu-brand" href="#">Bootsblogger</a>
    <div class="navmenu-nav">
      <a class="nav-item nav-link" href="#">Nav item</a>
      <a class="nav-item nav-link" href="#">Nav item again</a>
      <a class="nav-item nav-link" href="#">Another nav item</a>
    </div>
    <div class="navmenu-nav">
      <a class="nav-item nav-link active" href="#">Active</a>
      <a class="nav-item nav-link disabled" href="#">Disabled</a>
    </div>
  </nav>

  <nav class="navmenu navmenu-light" style="background-color: #e3f2fd; border-color: #b1deff;">
    <a class="navmenu-brand" href="#">Bootsblogger</a>
    <div class="navmenu-nav">
      <a class="nav-item nav-link" href="#">Nav item</a>
      <a class="nav-item nav-link" href="#">Nav item again</a>
      <a class="nav-item nav-link" href="#">Another nav item</a>
    </div>
    <div class="navmenu-nav">
      <a class="nav-item nav-link active" href="#">Active</a>
      <a class="nav-item nav-link disabled" href="#">Disabled</a>
    </div>
  </nav>
</div>

{% highlight html %}
<nav class="navmenu navmenu-dark bg-dark">
  <!-- Navmenu content -->
</nav>

<nav class="navmenu navmenu-dark bg-primary">
  <!-- Navmenu content -->
</nav>

<nav class="navmenu navmenu-light" style="background-color: #e3f2fd; border-color: #b1deff;">
  <!-- Navmenu content -->
</nav>
{% endhighlight %}

## Supported content

### Brand

As a link:

{% example html %}
<nav class="navmenu navmenu-light bg-light">
  <a class="navmenu-brand" href="#">Bootsblogger</a>
</nav>
{% endexample %}

As a heading:

{% example html %}
<nav class="navmenu navmenu-light bg-light">
  <span class="navmenu-brand h1 mb-0">Bootsblogger</span>
</nav>
{% endexample %}

Just an image:

{% example html %}
<nav class="navmenu navmenu-light bg-light">
  <a class="navmenu-brand text-center" href="#">
    <img src="{{ site.baseurl }}/assets/brand/bootsblogger-solid.svg" width="30" height="30" alt="">
  </a>
</nav>
{% endexample %}

Image and text:

{% example html %}
<nav class="navmenu navmenu-light bg-light">
  <a class="navmenu-brand" href="#">
    <img src="{{ site.baseurl }}/assets/brand/bootsblogger-solid.svg" width="30" height="30" alt="">
    <span class="ml-1">Bootsblogger</span>
  </a>
</nav>
{% endexample %}

### Nav

{% example html %}
<nav class="navmenu navmenu-light bg-light">
  <!-- 1 -->
  <div class="navmenu-nav">
    <a class="nav-item nav-link" href="#">Nav item</a>
    <a class="nav-item nav-link" href="#">Nav item again</a>
    <a class="nav-item nav-link" href="#">Another nav item</a>
  </div>

  <!-- 2 -->
  <div class="navmenu-nav">
    <div class="nav-item">
      <a class="nav-link" href="#">Nav item</a>
    </div>
    <div class="nav-item">
      <a class="nav-link" href="#">Nav item again</a>
    </div>
    <div class="nav-item">
      <a class="nav-link" href="#">Another nav item</a>
    </div>
  </div>

  <!-- 3 -->
  <ul class="navmenu-nav">
    <li class="nav-item">
      <a class="nav-link" href="#">Nav item</a>
    </li>
    <li class="nav-item">
      <a class="nav-link" href="#">Nav item again</a>
    </li>
    <li class="nav-item">
      <a class="nav-link" href="#">Another nav item</a>
    </li>
  </ul>
</nav>
{% endexample %}

**Small nav** - *Nav items* dengan *padding* atas dan bawah yang lebih kecil, tambahkan `.nav-link-sm` ke `.nav-link`:

{% example html %}
<nav class="navmenu navmenu-light bg-light">
  <div class="navmenu-nav">
    <a class="nav-item nav-link nav-link-sm" href="#">Nav item</a>
    <a class="nav-item nav-link nav-link-sm" href="#">Nav item again</a>
    <a class="nav-item nav-link nav-link-sm" href="#">Another nav item</a>
  </div>
</nav>
{% endexample %}

**Bordered nav** - *Nav items* dengan *border* atas dan bawah, tambahkan `.nav-item-bordered` ke `.nav-item`:

{% example html %}
<nav class="navmenu navmenu-light bg-light">
  <div class="navmenu-nav">
    <a class="nav-item nav-item-bordered nav-link" href="#">Nav item</a>
    <a class="nav-item nav-item-bordered nav-link" href="#">Nav item again</a>
    <a class="nav-item nav-item-bordered nav-link" href="#">Another nav item</a>
  </div>

  <div class="navmenu-nav">
    <div class="nav-item nav-item-bordered">
      <a class="nav-link" href="#">Nav item</a>
    </div>
    <div class="nav-item nav-item-bordered">
      <a class="nav-link" href="#">Nav item again</a>
    </div>
    <div class="nav-item nav-item-bordered">
      <a class="nav-link" href="#">Another nav item</a>
    </div>
  </div>
</nav>
{% endexample %}

**Hover** - Tambahkan `.nav-item-hover` ke `.nav-item`.

{% example html %}
<nav class="navmenu navmenu-light bg-light">
  <div class="navmenu-nav">
    <a class="nav-item nav-item-hover nav-link" href="#">Nav item</a>
    <a class="nav-item nav-item-hover nav-link" href="#">Nav item again</a>
    <a class="nav-item nav-item-hover nav-link" href="#">Another nav item</a>
    <a class="nav-item nav-item-hover nav-link active" href="#">Active</a>
    <a class="nav-item nav-item-hover nav-link disabled" href="#">Disabled</a>
  </div>

  <div class="navmenu-nav">
    <a class="nav-item nav-item-bordered nav-item-hover nav-link" href="#">Nav item</a>
    <a class="nav-item nav-item-bordered nav-item-hover nav-link" href="#">Nav item again</a>
    <a class="nav-item nav-item-bordered nav-item-hover nav-link" href="#">Another nav item</a>
    <a class="nav-item nav-item-bordered nav-item-hover nav-link active" href="#">Active</a>
    <a class="nav-item nav-item-bordered nav-item-hover nav-link disabled" href="#">Disabled</a>
  </div>

  <div class="navmenu-nav">
    <div class="nav-item nav-item-hover">
      <a class="nav-link" href="#">Nav item</a>
    </div>
    <div class="nav-item nav-item-hover">
      <a class="nav-link" href="#">Nav item again</a>
    </div>
    <div class="nav-item nav-item-hover">
      <a class="nav-link" href="#">Another nav item</a>
    </div>
    <div class="nav-item nav-item-hover">
      <a class="nav-link active" href="#">Active</a>
    </div>
    <div class="nav-item nav-item-hover">
      <a class="nav-link disabled" href="#">Disabled</a>
    </div>
  </div>

  <div class="navmenu-nav">
    <div class="nav-item nav-item-bordered nav-item-hover">
      <a class="nav-link" href="#">Nav item</a>
    </div>
    <div class="nav-item nav-item-bordered nav-item-hover">
      <a class="nav-link" href="#">Nav item again</a>
    </div>
    <div class="nav-item nav-item-bordered nav-item-hover">
      <a class="nav-link" href="#">Another nav item</a>
    </div>
    <div class="nav-item nav-item-bordered nav-item-hover">
      <a class="nav-link active" href="#">Active</a>
    </div>
    <div class="nav-item nav-item-bordered nav-item-hover">
      <a class="nav-link disabled" href="#">Disabled</a>
    </div>
  </div>
</nav>
{% endexample %}

### Headers

{% example html %}
<nav class="navmenu navmenu-light bg-light">
  <h6 class="navmenu-header">Header</h6>
  <div class="navmenu-nav">
    <a class="nav-item nav-link" href="#">Nav item</a>
    <a class="nav-item nav-link" href="#">Nav item again</a>
    <a class="nav-item nav-link" href="#">Another nav item</a>
  </div>
</nav>
{% endexample %}

### Dividers

{% example html %}
<nav class="navmenu navmenu-light bg-light">
  <div class="navmenu-nav">
    <a class="nav-item nav-link" href="#">Nav item</a>
    <a class="nav-item nav-link" href="#">Nav item again</a>
    <a class="nav-item nav-link" href="#">Another nav item</a>
  </div>

  <div class="navmenu-divider"></div>

  <div class="navmenu-nav">
    <a class="nav-item nav-link" href="#">Nav item</a>
    <a class="nav-item nav-link" href="#">Nav item again</a>
    <a class="nav-item nav-link" href="#">Another nav item</a>
  </div>
</nav>
{% endexample %}

### With `.navmenu-content`

Gunakan `.navmenu-content` untuk membuat elemen lainnya, lihat beberapa contoh berikut:

{% example html %}
<nav class="navmenu navmenu-light bg-light">
  <div class="navmenu-content">
    <form>
      <input class="form-control" type="text" placeholder="Search for..." aria-label="Search for...">
    </form>
  </div>
</nav>
{% endexample %}

{% example html %}
<nav class="navmenu navmenu-light bg-light">
  <div class="navmenu-content">
    <form class="d-flex align-items-center">
      <input class="form-control" type="text" placeholder="Search for..." aria-label="Search for...">
      <button class="btn btn-primary ml-2" type="submit">Go!</button>
    </form>
  </div>
</nav>
{% endexample %}

{% example html %}
<nav class="navmenu navmenu-light bg-light">
  <div class="navmenu-content">
    <a class="btn btn-block btn-primary" href="#">Go somewhere</a>
  </div>
</nav>
{% endexample %}

{% example html %}
<nav class="navmenu navmenu-light bg-light">
  <div class="navmenu-content">
    <p class="text-success mb-0">Hello, world!</p>
  </div>
</nav>
{% endexample %}

### Mix and match

{% example html %}
<nav class="navmenu navmenu-light bg-light">
  <a class="navmenu-brand" href="#">Bootsblogger</a>

  <div class="navmenu-divider"></div>

  <h6 class="navmenu-header">Nav</h6>
  <div class="navmenu-nav">
    <a class="nav-item nav-link" href="#">Nav item</a>
    <a class="nav-item nav-link" href="#">Nav item again</a>
    <a class="nav-item nav-link" href="#">Another nav item</a>
  </div>

  <div class="navmenu-divider"></div>

  <h6 class="navmenu-header">Form</h6>
  <div class="navmenu-content">
    <form>
      <input class="form-control" type="text" placeholder="Search for..." aria-label="Search for...">
    </form>
  </div>

  <div class="navmenu-divider"></div>

  <h6 class="navmenu-header">Button</h6>
  <div class="navmenu-content d-flex flex-wrap flex-column">
    <div class="btn-group">
      <a class="btn btn-secondary w-100" href="#">Action 1</a>
      <a class="btn btn-secondary w-100" href="#">Action 2</a>
    </div>
  </div>

  <div class="navmenu-divider"></div>

  <h6 class="navmenu-header">Text</h6>
  <div class="navmenu-content">
    <p class="text-muted mb-0">Donec id elit non mi porta gravida at eget metus. Maecenas sed diam eget risus varius blandit.</p>
  </div>
</nav>
{% endexample %}

{% example html %}
<nav class="navmenu navmenu-dark bg-dark">
  <a class="navmenu-brand" href="#">Bootsblogger</a>

  <div class="navmenu-divider"></div>

  <h6 class="navmenu-header">Nav</h6>
  <div class="navmenu-nav">
    <a class="nav-item nav-link" href="#">Nav item</a>
    <a class="nav-item nav-link" href="#">Nav item again</a>
    <a class="nav-item nav-link" href="#">Another nav item</a>
  </div>

  <div class="navmenu-divider"></div>

  <h6 class="navmenu-header">Form</h6>
  <div class="navmenu-content">
    <form>
      <input class="form-control" type="text" placeholder="Search for..." aria-label="Search for...">
    </form>
  </div>

  <div class="navmenu-divider"></div>

  <h6 class="navmenu-header">Button</h6>
  <div class="navmenu-content d-flex flex-wrap flex-column">
    <div class="btn-group">
      <a class="btn btn-primary w-100" href="#">Action 1</a>
      <a class="btn btn-primary w-100" href="#">Action 2</a>
    </div>
  </div>

  <div class="navmenu-divider"></div>

  <h6 class="navmenu-header">Text</h6>
  <div class="navmenu-content">
    <p class="text-light mb-0">Donec id elit non mi porta gravida at eget metus. Maecenas sed diam eget risus varius blandit.</p>
  </div>
</nav>
{% endexample %}

## Collapse

Example 1:

{% example html %}
<nav class="navmenu navmenu-light bg-light">
  <a class="navmenu-brand" href="#">Bootsblogger</a>
  <div class="navmenu-nav">
    <a class="nav-item nav-link nav-link-collapse collapsed" data-toggle="collapse" href="#navmenuNavCollapseDemo01" aria-expanded="false" aria-controls="navmenuNavCollapseDemo01">
      Nav item collapse
    </a>
    <div class="collapse" id="navmenuNavCollapseDemo01">
      <div style="border-left: 4px solid #ddd;">
        <a class="nav-item nav-link nav-link-sm small" href="#">Nav item</a>
        <a class="nav-item nav-link nav-link-sm small" href="#">Nav item again</a>
        <a class="nav-item nav-link nav-link-sm small" href="#">Another nav item</a>
      </div>
    </div>
    <a class="nav-item nav-link" href="#">Nav item again</a>
    <a class="nav-item nav-link" href="#">Another nav item</a>
  </div>
</nav>
{% endexample %}

Example 2:

{% example html %}
<nav class="navmenu navmenu-light bg-light">
  <a class="navmenu-brand" href="#">Bootsblogger</a>
  <div class="navmenu-nav">
    <a class="nav-item nav-link nav-link-collapse collapsed" data-toggle="collapse" href="#navmenuNavCollapseDemo02" aria-expanded="false" aria-controls="navmenuNavCollapseDemo02">
      Nav item collapse
    </a>
    <div class="collapse" id="navmenuNavCollapseDemo02">
      <div>
        <a class="nav-item nav-item-bordered nav-item-hover nav-link nav-link-sm small" href="#">Nav item</a>
        <a class="nav-item nav-item-bordered nav-item-hover nav-link nav-link-sm small" href="#">Nav item again</a>
        <a class="nav-item nav-item-bordered nav-item-hover nav-link nav-link-sm small" href="#">Another nav item</a>
      </div>
    </div>
    <a class="nav-item nav-link" href="#">Nav item again</a>
    <a class="nav-item nav-link" href="#">Another nav item</a>
  </div>
</nav>
{% endexample %}

Example 3:

{% example html %}
<nav class="navmenu navmenu-dark bg-dark">
  <a class="navmenu-brand" href="#">Bootsblogger</a>
  <div class="navmenu-nav">
    <div class="nav-item nav-item-bordered">
      <a class="nav-link nav-link-collapse collapsed" data-toggle="collapse" href="#navmenuNavCollapseDemo03" aria-expanded="false" aria-controls="navmenuNavCollapseDemo03">
        Nav item collapse
      </a>
      <div class="collapse" id="navmenuNavCollapseDemo03">
        <div class="mb-2">
          <a class="nav-item nav-link nav-link-sm small" href="#">Nav item</a>
          <a class="nav-item nav-link nav-link-sm small" href="#">Nav item again</a>
          <a class="nav-item nav-link nav-link-sm small" href="#">Another nav item</a>
        </div>
      </div>
    </div>
    <div class="nav-item nav-item-bordered">
      <a class="nav-link" href="#">Nav item again</a>
    </div>
    <div class="nav-item nav-item-bordered">
      <a class="nav-link" href="#">Another nav item</a>
    </div>
  </div>
</nav>
{% endexample %}

## Dropdowns

{% example html %}
<nav class="navmenu navmenu-light bg-light">
  <a class="navmenu-brand" href="#">Bootsblogger</a>
  <ul class="navmenu-nav">
    <li class="nav-item"><a class="nav-link" href="#">Nav item</a></li>
    <li class="nav-item"><a class="nav-link" href="#">Nav item again</a></li>
    <li class="nav-item dropdown">
      <a class="nav-link dropdown-toggle" href="#" id="navmenuDropdownMenuLink" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
        Dropdown link
      </a>
      <div class="dropdown-menu" aria-labelledby="navmenuDropdownMenuLink">
        <a class="dropdown-item" href="#">Action</a>
        <a class="dropdown-item" href="#">Another action</a>
        <a class="dropdown-item" href="#">Something else here</a>
      </div>
    </li>
    <li class="nav-item dropup">
      <a class="nav-link dropdown-toggle" href="#" id="navmenuDropupMenuLink" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
        Dropup
      </a>
      <div class="dropdown-menu" aria-labelledby="navmenuDropupMenuLink">
        <a class="dropdown-item" href="#">Action</a>
        <a class="dropdown-item" href="#">Another action</a>
        <a class="dropdown-item" href="#">Something else here</a>
      </div>
    </li>
  </ul>
</nav>
{% endexample %}

## Placement

{% example html %}
<nav class="navmenu navmenu-fixed-left navmenu-light bg-light" style="width: 15rem;">
  <a class="navmenu-brand" href="#">Fixed left</a>
  <div class="navmenu-nav">
    <a class="nav-item nav-link" href="#">Nav item</a>
    <a class="nav-item nav-link" href="#">Nav item again</a>
    <a class="nav-item nav-link" href="#">Another nav item</a>
  </div>
</nav>
{% endexample %}

{% example html %}
<nav class="navmenu navmenu-fixed-right navmenu-light bg-light" style="width: 15rem;">
  <a class="navmenu-brand" href="#">Fixed right</a>
  <div class="navmenu-nav">
    <a class="nav-item nav-link" href="#">Nav item</a>
    <a class="nav-item nav-link" href="#">Nav item again</a>
    <a class="nav-item nav-link" href="#">Another nav item</a>
  </div>
</nav>
{% endexample %}

## Responsive behaviors

Dengan menggunakan `.navmenu-toggler`, `.navmenu-collapse`, dan `.navmenu-expand{-sm|-md|-lg|-xl}` Anda dapat menentukan kapan menampilkan atau menyembunyikan elemen navmenu.

Kelas untuk `xs` tidak tersedia (`.navmenu-expand`).

### Toggler

`xs`:

Tidak membutuhkan `.navmenu-expand`, `.navmenu-toggler`, dan `.navmenu-collapse`.

{% example html %}
<nav class="navmenu navmenu-light bg-light">
  <div class="navmenu-content">
    <button class="btn btn-secondary btn-block" type="button" data-toggle="collapse" data-target="#navmenuTogglerDemo0" aria-controls="navmenuTogglerDemo0" aria-expanded="false" aria-label="Toggle navigation">Toggle nav</button>
  </div>

  <div class="collapse" id="navmenuTogglerDemo0">
    <div class="navmenu-nav mt-3">
      <a class="nav-item nav-link" href="#">Nav item</a>
      <a class="nav-item nav-link" href="#">Nav item again</a>
      <a class="nav-item nav-link" href="#">Another nav item</a>
    </div>
  </div>
</nav>
{% endexample %}

`sm` (&lt;576px):

{% example html %}
<nav class="navmenu navmenu-expand-sm navmenu-light bg-light">
  <div class="navmenu-content navmenu-toggler">
    <button class="btn btn-secondary btn-block" type="button" data-toggle="collapse" data-target="#navmenuTogglerDemo01" aria-controls="navmenuTogglerDemo01" aria-expanded="false" aria-label="Toggle navigation">Toggle nav</button>
  </div>

  <div class="collapse navmenu-collapse" id="navmenuTogglerDemo01">
    <div class="navmenu-nav mt-3 mt-sm-0">
      <a class="nav-item nav-link" href="#">Nav item</a>
      <a class="nav-item nav-link" href="#">Nav item again</a>
      <a class="nav-item nav-link" href="#">Another nav item</a>
    </div>
  </div>
</nav>
{% endexample %}

`md` (&lt;768px):

{% example html %}
<nav class="navmenu navmenu-expand-md navmenu-light bg-light">
  <div class="navmenu-content navmenu-toggler">
    <button class="btn btn-secondary btn-block" type="button" data-toggle="collapse" data-target="#navmenuTogglerDemo02" aria-controls="navmenuTogglerDemo02" aria-expanded="false" aria-label="Toggle navigation">Toggle nav</button>
  </div>

  <div class="collapse navmenu-collapse" id="navmenuTogglerDemo02">
    <div class="navmenu-nav mt-3 mt-md-0">
      <a class="nav-item nav-link" href="#">Nav item</a>
      <a class="nav-item nav-link" href="#">Nav item again</a>
      <a class="nav-item nav-link" href="#">Another nav item</a>
    </div>
  </div>
</nav>
{% endexample %}

`lg` (&lt;992px):

{% example html %}
<nav class="navmenu navmenu-expand-lg navmenu-light bg-light">
  <div class="navmenu-content navmenu-toggler">
    <button class="btn btn-secondary btn-block" type="button" data-toggle="collapse" data-target="#navmenuTogglerDemo03" aria-controls="navmenuTogglerDemo03" aria-expanded="false" aria-label="Toggle navigation">Toggle nav</button>
  </div>

  <div class="collapse navmenu-collapse" id="navmenuTogglerDemo03">
    <div class="navmenu-nav mt-3 mt-lg-0">
      <a class="nav-item nav-link" href="#">Nav item</a>
      <a class="nav-item nav-link" href="#">Nav item again</a>
      <a class="nav-item nav-link" href="#">Another nav item</a>
    </div>
  </div>
</nav>
{% endexample %}

`xl` (&lt;1200px):

{% example html %}
<nav class="navmenu navmenu-expand-xl navmenu-light bg-light">
  <div class="navmenu-content navmenu-toggler">
    <button class="btn btn-secondary btn-block" type="button" data-toggle="collapse" data-target="#navmenuTogglerDemo04" aria-controls="navmenuTogglerDemo04" aria-expanded="false" aria-label="Toggle navigation">Toggle nav</button>
  </div>

  <div class="collapse navmenu-collapse" id="navmenuTogglerDemo04">
    <div class="navmenu-nav mt-3 mt-xl-0">
      <a class="nav-item nav-link" href="#">Nav item</a>
      <a class="nav-item nav-link" href="#">Nav item again</a>
      <a class="nav-item nav-link" href="#">Another nav item</a>
    </div>
  </div>
</nav>
{% endexample %}
