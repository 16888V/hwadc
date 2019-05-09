---
layout: docs
title: Widget
description: Komponen untuk tampilan widget/gadget.
group: components
toc: true
---

## Base class

Komponen widget membutuhkan penggunaan kelas dasar `.wg` untuk mengatur *margin* dan ukuran judul widget (dapat diubah menggunakan kelas pengubah [ukuran judul widget](#font-size)).

**Catatan:** komponen widget tidak mengubah warna konten yang berada di dalamnya (di dalam `.widget-content`), oleh karena itu, Anda perlu menyesuaikannya dengan *custom styles* atau kelas utilitas.

<div class="bd-example">
  <div class="wg">
    <div class="widget">
      <h4 class="title">Widget title</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
</div><!-- /.bd-example -->

{% highlight html %}
<b:section class='wg' id='sectionId'></b:section>
{% endhighlight %}

## Title

Kelas-kelas untuk mengatur judul widget—warna, ukuran, perataan, dan kelas untuk menyembunyikan judul widget.

### Color

Kelas-kelas yang tersedia untuk mengubah warna judul widget.

<div class="bd-example bd-example-widget-inverse text-white">
  <div class="wg wg-title-light">
    <div class="widget">
      <h4 class="title">Light</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-title-dark">
    <div class="widget">
      <h4 class="title">Dark</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-title-white">
    <div class="widget">
      <h4 class="title">White</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-title-black">
    <div class="widget">
      <h4 class="title">Black</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-title-blue">
    <div class="widget">
      <h4 class="title">Blue</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-title-indigo">
    <div class="widget">
      <h4 class="title">Indigo</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-title-purple">
    <div class="widget">
      <h4 class="title">Purple</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-title-pink">
    <div class="widget">
      <h4 class="title">Pink</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-title-red">
    <div class="widget">
      <h4 class="title">Red</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-title-orange">
    <div class="widget">
      <h4 class="title">Orange</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-title-yellow">
    <div class="widget">
      <h4 class="title">Yellow</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-title-green">
    <div class="widget">
      <h4 class="title">Green</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-title-teal">
    <div class="widget">
      <h4 class="title">Teal</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-title-cyan">
    <div class="widget">
      <h4 class="title">Cyan</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
</div><!-- /.bd-example -->

{% highlight html %}
<b:section class='wg wg-title-light' id='sectionId'></b:section>
<b:section class='wg wg-title-dark' id='sectionId'></b:section>
<b:section class='wg wg-title-white' id='sectionId'></b:section>
<b:section class='wg wg-title-black' id='sectionId'></b:section>
<b:section class='wg wg-title-blue' id='sectionId'></b:section>
<b:section class='wg wg-title-indigo' id='sectionId'></b:section>
<b:section class='wg wg-title-purple' id='sectionId'></b:section>
<b:section class='wg wg-title-pink' id='sectionId'></b:section>
<b:section class='wg wg-title-red' id='sectionId'></b:section>
<b:section class='wg wg-title-orange' id='sectionId'></b:section>
<b:section class='wg wg-title-yellow' id='sectionId'></b:section>
<b:section class='wg wg-title-green' id='sectionId'></b:section>
<b:section class='wg wg-title-teal' id='sectionId'></b:section>
<b:section class='wg wg-title-cyan' id='sectionId'></b:section>
{% endhighlight %}

### Font size

Untuk mengubah ukuran judul widget gunakan `.wg-title{-h1|-h2|-h4|-h4|-h5|-h6}`.

<div class="bd-example">
  <div class="wg wg-title-h1">
    <div class="widget">
      <h4 class="title">H1. Widget title</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-title-h2">
    <div class="widget">
      <h4 class="title">H2. Widget title</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-title-h4">
    <div class="widget">
      <h4 class="title">H3. Widget title</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-title-h4">
    <div class="widget">
      <h4 class="title">H4. Widget title</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-title-h5">
    <div class="widget">
      <h4 class="title">H5. Widget title</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-title-h6">
    <div class="widget">
      <h4 class="title">H6. Widget title</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
</div><!-- /.bd-example -->

{% highlight html %}
<b:section class='wg wg-title-h1' id='sectionId'></b:section>
<b:section class='wg wg-title-h2' id='sectionId'></b:section>
<b:section class='wg wg-title-h4' id='sectionId'></b:section>
<b:section class='wg wg-title-h4' id='sectionId'></b:section>
<b:section class='wg wg-title-h5' id='sectionId'></b:section>
<b:section class='wg wg-title-h6' id='sectionId'></b:section>
{% endhighlight %}

### Alignment

Terdapat tiga kelas untuk perataan judul widget, yaitu rata kiri `.wg-title-left`, rata tengah `.wg-title-center`, dan rata kanan `.wg-title-right`.

<div class="bd-example">
  <div class="wg wg-title-left">
    <div class="widget">
      <h4 class="title">Left</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-title-center">
    <div class="widget">
      <h4 class="title">Center</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-title-right">
    <div class="widget">
      <h4 class="title">Right</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
</div><!-- /.bd-example -->

{% highlight html %}
<b:section class='wg wg-title-left' id='sectionId'></b:section>
<b:section class='wg wg-title-center' id='sectionId'></b:section>
<b:section class='wg wg-title-right' id='sectionId'></b:section>
{% endhighlight %}

### Hide

Untuk menyembunyikan judul widget gunakan `.wg-title-hide`.

<div class="bd-example">
  <div class="wg wg-title-hide">
    <div class="widget">
      <h4 class="title">Hidden</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
</div><!-- /.bd-example -->

{% highlight html %}
<b:section class='wg wg-title-hide' id='sectionId'></b:section>
{% endhighlight %}

## Widget box

### Basic example

Gunakan `.wg-box`, `.wg-box-{color}`, dan [`.wg-title-{color}`](#color).

<div class="bd-example bd-example-widget-inverse text-muted">
  <div class="wg wg-box wg-box-light wg-title-dark">
    <div class="widget">
      <h4 class="title">Light</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-box wg-box-dark wg-title-light">
    <div class="widget">
      <h4 class="title">Dark</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-box wg-box-white wg-title-black">
    <div class="widget">
      <h4 class="title">White</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-box wg-box-black wg-title-white">
    <div class="widget">
      <h4 class="title">Black</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-box wg-box-blue wg-title-white">
    <div class="widget">
      <h4 class="title">Blue</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-box wg-box-indigo wg-title-white">
    <div class="widget">
      <h4 class="title">Indigo</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-box wg-box-purple wg-title-white">
    <div class="widget">
      <h4 class="title">Purple</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-box wg-box-pink wg-title-white">
    <div class="widget">
      <h4 class="title">Pink</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-box wg-box-red wg-title-white">
    <div class="widget">
      <h4 class="title">Red</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-box wg-box-orange wg-title-white">
    <div class="widget">
      <h4 class="title">Orange</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-box wg-box-yellow wg-title-white">
    <div class="widget">
      <h4 class="title">Yellow</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-box wg-box-green wg-title-white">
    <div class="widget">
      <h4 class="title">Green</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-box wg-box-teal wg-title-white">
    <div class="widget">
      <h4 class="title">Teal</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-box wg-box-cyan wg-title-white">
    <div class="widget">
      <h4 class="title">Cyan</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
</div><!-- /.bd-example -->

{% highlight html %}
<b:section class='wg wg-box wg-box-light wg-title-dark' id='sectionId'></b:section>
<b:section class='wg wg-box wg-box-dark wg-title-light' id='sectionId'></b:section>
<b:section class='wg wg-box wg-box-white wg-title-black' id='sectionId'></b:section>
<b:section class='wg wg-box wg-box-black wg-title-white' id='sectionId'></b:section>
<b:section class='wg wg-box wg-box-blue wg-title-white' id='sectionId'></b:section>
<b:section class='wg wg-box wg-box-indigo wg-title-white' id='sectionId'></b:section>
<b:section class='wg wg-box wg-box-purple wg-title-white' id='sectionId'></b:section>
<b:section class='wg wg-box wg-box-pink wg-title-white' id='sectionId'></b:section>
<b:section class='wg wg-box wg-box-red wg-title-white' id='sectionId'></b:section>
<b:section class='wg wg-box wg-box-orange wg-title-white' id='sectionId'></b:section>
<b:section class='wg wg-box wg-box-yellow wg-title-white' id='sectionId'></b:section>
<b:section class='wg wg-box wg-box-green wg-title-white' id='sectionId'></b:section>
<b:section class='wg wg-box wg-box-teal wg-title-white' id='sectionId'></b:section>
<b:section class='wg wg-box wg-box-cyan wg-title-white' id='sectionId'></b:section>
{% endhighlight %}

### Outline

Ubah `.wg-box-{color}` menjadi `.wg-box-outline-{color}`.

<div class="bd-example bd-example-widget-inverse text-white">
  <div class="wg wg-box wg-box-outline-light wg-title-light">
    <div class="widget">
      <h4 class="title">Light</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-box wg-box-outline-dark wg-title-dark">
    <div class="widget">
      <h4 class="title">Dark</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-box wg-box-outline-white wg-title-white">
    <div class="widget">
      <h4 class="title">White</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-box wg-box-outline-black wg-title-black">
    <div class="widget">
      <h4 class="title">Black</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-box wg-box-outline-blue wg-title-blue">
    <div class="widget">
      <h4 class="title">Blue</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-box wg-box-outline-indigo wg-title-indigo">
    <div class="widget">
      <h4 class="title">Indigo</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-box wg-box-outline-purple wg-title-purple">
    <div class="widget">
      <h4 class="title">Purple</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-box wg-box-outline-pink wg-title-pink">
    <div class="widget">
      <h4 class="title">Pink</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-box wg-box-outline-red wg-title-red">
    <div class="widget">
      <h4 class="title">Red</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-box wg-box-outline-orange wg-title-orange">
    <div class="widget">
      <h4 class="title">Orange</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-box wg-box-outline-yellow wg-title-yellow">
    <div class="widget">
      <h4 class="title">Yellow</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-box wg-box-outline-green wg-title-green">
    <div class="widget">
      <h4 class="title">Green</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-box wg-box-outline-teal wg-title-teal">
    <div class="widget">
      <h4 class="title">Teal</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-box wg-box-outline-cyan wg-title-cyan">
    <div class="widget">
      <h4 class="title">Cyan</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
</div><!-- /.bd-example -->

{% highlight html %}
<b:section class='wg wg-box wg-box-outline-{color} wg-title-{color}' id='sectionId'></b:section>
{% endhighlight %}

### List groups

*Flush list group* di dalam widget-box.

<div class="bd-example">
  <div class="wg wg-box wg-box-white wg-title-dark">
    <div class="widget">
      <h4 class="title">Widget title</h4>
      <div class="widget-content">
        <div class="list-group list-group-flush">
          <a class="list-group-item list-group-item-action" href="#">Cras justo odio</a>
          <a class="list-group-item list-group-item-action" href="#">Dapibus ac facilisis in</a>
          <a class="list-group-item list-group-item-action" href="#">Morbi leo risus</a>
          <a class="list-group-item list-group-item-action" href="#">Porta ac consectetur ac</a>
          <a class="list-group-item list-group-item-action" href="#">Vestibulum at eros</a>
        </div>
      </div>
    </div><!-- /.widget -->
    <div class="widget">
      <h4 class="title">Widget title</h4>
      <div class="widget-content">
        <p><code>&lt;p&gt;...&lt;/p&gt;</code></p>
        <div class="list-group list-group-flush">
          <a class="list-group-item list-group-item-action" href="#">Cras justo odio</a>
          <a class="list-group-item list-group-item-action" href="#">Dapibus ac facilisis in</a>
          <a class="list-group-item list-group-item-action" href="#">Morbi leo risus</a>
          <a class="list-group-item list-group-item-action" href="#">Porta ac consectetur ac</a>
          <a class="list-group-item list-group-item-action" href="#">Vestibulum at eros</a>
        </div>
        <p class="mt-3"><code>&lt;p class="mt-3"&gt;...&lt;/p&gt;</code></p>
      </div>
    </div><!-- /.widget -->
  </div>
</div><!-- /.bd-example -->

{% highlight html %}
<b:section class='wg wg-box wg-box-white wg-title-dark' id='sectionId'></b:section>
{% endhighlight %}

Markup:

{% highlight html %}
<div class="list-group list-group-flush">
  <a class="list-group-item list-group-item-action" href="#">Cras justo odio</a>
  <a class="list-group-item list-group-item-action" href="#">Dapibus ac facilisis in</a>
  <a class="list-group-item list-group-item-action" href="#">Morbi leo risus</a>
  <a class="list-group-item list-group-item-action" href="#">Porta ac consectetur ac</a>
  <a class="list-group-item list-group-item-action" href="#">Vestibulum at eros</a>
</div>
{% endhighlight %}

## Widget panel

### Basic example

Gunakan `.wg-panel`, `.wg-panel-{color}`, dan [`.wg-title-{color}`](#color).

<div class="bd-example bd-example-widget-inverse text-dark">
  <div class="wg wg-panel wg-panel-light wg-title-dark">
    <div class="widget">
      <h4 class="title">Light</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-panel wg-panel-dark wg-title-light">
    <div class="widget">
      <h4 class="title">Dark</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-panel wg-panel-white wg-title-black">
    <div class="widget">
      <h4 class="title">White</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-panel wg-panel-black wg-title-white">
    <div class="widget">
      <h4 class="title">Black</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-panel wg-panel-blue wg-title-white">
    <div class="widget">
      <h4 class="title">Blue</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-panel wg-panel-indigo wg-title-white">
    <div class="widget">
      <h4 class="title">Indigo</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-panel wg-panel-purple wg-title-white">
    <div class="widget">
      <h4 class="title">Purple</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-panel wg-panel-pink wg-title-white">
    <div class="widget">
      <h4 class="title">Pink</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-panel wg-panel-red wg-title-white">
    <div class="widget">
      <h4 class="title">Red</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-panel wg-panel-orange wg-title-white">
    <div class="widget">
      <h4 class="title">Orange</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-panel wg-panel-yellow wg-title-white">
    <div class="widget">
      <h4 class="title">Yellow</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-panel wg-panel-green wg-title-white">
    <div class="widget">
      <h4 class="title">Green</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-panel wg-panel-teal wg-title-white">
    <div class="widget">
      <h4 class="title">Teal</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-panel wg-panel-cyan wg-title-white">
    <div class="widget">
      <h4 class="title">Cyan</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
</div><!-- /.bd-example -->

{% highlight html %}
<b:section class='wg wg-panel wg-panel-light wg-title-dark' id='sectionId'></b:section>
<b:section class='wg wg-panel wg-panel-dark wg-title-light' id='sectionId'></b:section>
<b:section class='wg wg-panel wg-panel-white wg-title-black' id='sectionId'></b:section>
<b:section class='wg wg-panel wg-panel-black wg-title-white' id='sectionId'></b:section>
<b:section class='wg wg-panel wg-panel-blue wg-title-white' id='sectionId'></b:section>
<b:section class='wg wg-panel wg-panel-indigo wg-title-white' id='sectionId'></b:section>
<b:section class='wg wg-panel wg-panel-purple wg-title-white' id='sectionId'></b:section>
<b:section class='wg wg-panel wg-panel-pink wg-title-white' id='sectionId'></b:section>
<b:section class='wg wg-panel wg-panel-red wg-title-white' id='sectionId'></b:section>
<b:section class='wg wg-panel wg-panel-orange wg-title-white' id='sectionId'></b:section>
<b:section class='wg wg-panel wg-panel-yellow wg-title-white' id='sectionId'></b:section>
<b:section class='wg wg-panel wg-panel-green wg-title-white' id='sectionId'></b:section>
<b:section class='wg wg-panel wg-panel-teal wg-title-white' id='sectionId'></b:section>
<b:section class='wg wg-panel wg-panel-cyan wg-title-white' id='sectionId'></b:section>
{% endhighlight %}

### Outline

Ubah `.wg-panel-{color}` menjadi `.wg-panel-outline-{color}`.

<div class="bd-example bd-example-widget-inverse text-white">
  <div class="wg wg-panel wg-panel-outline-light wg-title-light">
    <div class="widget">
      <h4 class="title">Light</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-panel wg-panel-outline-dark wg-title-dark">
    <div class="widget">
      <h4 class="title">Dark</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-panel wg-panel-outline-white wg-title-white">
    <div class="widget">
      <h4 class="title">White</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-panel wg-panel-outline-black wg-title-black">
    <div class="widget">
      <h4 class="title">Black</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-panel wg-panel-outline-blue wg-title-blue">
    <div class="widget">
      <h4 class="title">Blue</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-panel wg-panel-outline-indigo wg-title-indigo">
    <div class="widget">
      <h4 class="title">Indigo</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-panel wg-panel-outline-purple wg-title-purple">
    <div class="widget">
      <h4 class="title">Purple</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-panel wg-panel-outline-pink wg-title-pink">
    <div class="widget">
      <h4 class="title">Pink</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-panel wg-panel-outline-red wg-title-red">
    <div class="widget">
      <h4 class="title">Red</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-panel wg-panel-outline-orange wg-title-orange">
    <div class="widget">
      <h4 class="title">Orange</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-panel wg-panel-outline-yellow wg-title-yellow">
    <div class="widget">
      <h4 class="title">Yellow</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-panel wg-panel-outline-green wg-title-green">
    <div class="widget">
      <h4 class="title">Green</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-panel wg-panel-outline-teal wg-title-teal">
    <div class="widget">
      <h4 class="title">Teal</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
  <div class="wg wg-panel wg-panel-outline-cyan wg-title-cyan">
    <div class="widget">
      <h4 class="title">Cyan</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
</div><!-- /.bd-example -->

{% highlight html %}
<b:section class='wg wg-panel wg-panel-outline-{color} wg-title-{color}' id='sectionId'></b:section>
{% endhighlight %}

### Smaller

Tambahkan `.wg-panel-sm`.

<div class="bd-example">
  <div class="wg wg-panel wg-panel-sm wg-panel-orange wg-title-dark">
    <div class="widget">
      <h4 class="title">Widget title</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
</div><!-- /.bd-example -->

{% highlight html %}
<b:section class='wg wg-panel wg-panel-sm wg-panel-orange wg-title-dark' id='sectionId'></b:section>
{% endhighlight %}

### Group

Tambahkan `.wg-panel-group`.

<div class="bd-example">
  <div class="wg wg-panel wg-panel-group wg-panel-teal wg-title-white">
    <div class="widget">
      <h4 class="title">Widget title</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
    <div class="widget">
      <h4 class="title">Widget title</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
    <div class="widget">
      <h4 class="title">Widget title</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
</div><!-- /.bd-example -->

{% highlight html %}
<b:section class='wg wg-panel wg-panel-group wg-panel-teal wg-title-white' id='sectionId'></b:section>
{% endhighlight %}

### List groups

*Flush list group* di dalam widget-panel.

<div class="bd-example">
  <div class="wg wg-panel wg-panel-purple wg-title-white">
    <div class="widget">
      <h4 class="title">Widget title</h4>
      <div class="widget-content">
        <div class="list-group list-group-flush">
          <a class="list-group-item list-group-item-action" href="#">Cras justo odio</a>
          <a class="list-group-item list-group-item-action" href="#">Dapibus ac facilisis in</a>
          <a class="list-group-item list-group-item-action" href="#">Morbi leo risus</a>
          <a class="list-group-item list-group-item-action" href="#">Porta ac consectetur ac</a>
          <a class="list-group-item list-group-item-action" href="#">Vestibulum at eros</a>
        </div>
      </div>
    </div><!-- /.widget -->
    <div class="widget">
      <h4 class="title">Widget title</h4>
      <div class="widget-content">
        <p><code>&lt;p&gt;...&lt;/p&gt;</code></p>
        <div class="list-group list-group-flush">
          <a class="list-group-item list-group-item-action" href="#">Cras justo odio</a>
          <a class="list-group-item list-group-item-action" href="#">Dapibus ac facilisis in</a>
          <a class="list-group-item list-group-item-action" href="#">Morbi leo risus</a>
          <a class="list-group-item list-group-item-action" href="#">Porta ac consectetur ac</a>
          <a class="list-group-item list-group-item-action" href="#">Vestibulum at eros</a>
        </div>
        <p class="mt-3"><code>&lt;p class="mt-3"&gt;...&lt;/p&gt;</code></p>
      </div>
    </div><!-- /.widget -->
  </div>
</div><!-- /.bd-example -->

{% highlight html %}
<b:section class='wg wg-panel wg-panel-purple wg-title-white' id='sectionId'></b:section>
{% endhighlight %}

Markup:

{% highlight html %}
<div class="list-group list-group-flush">
  <a class="list-group-item list-group-item-action" href="#">Cras justo odio</a>
  <a class="list-group-item list-group-item-action" href="#">Dapibus ac facilisis in</a>
  <a class="list-group-item list-group-item-action" href="#">Morbi leo risus</a>
  <a class="list-group-item list-group-item-action" href="#">Porta ac consectetur ac</a>
  <a class="list-group-item list-group-item-action" href="#">Vestibulum at eros</a>
</div>
{% endhighlight %}

## Grid

Sistem grid untuk widget.

### Options

<table class="table table-bordered table-striped table-responsive">
  <thead>
    <tr>
      <th></th>
      <th class="text-center">
        Extra small<br>
        <small>&lt;576px</small>
      </th>
      <th class="text-center">
        Small<br>
        <small>&ge;576px</small>
      </th>
      <th class="text-center">
        Medium<br>
        <small>&ge;768px</small>
      </th>
      <th class="text-center">
        Large<br>
        <small>&ge;992px</small>
      </th>
      <th class="text-center">
        Extra large<br>
        <small>&ge;1200px</small>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th class="text-nowrap" scope="row">Grid behavior</th>
      <td>Horizontal at all times</td>
      <td colspan="4">Collapsed to start, horizontal above breakpoints</td>
    </tr>
    <tr>
      <th class="text-nowrap" scope="row">Class prefix</th>
      <td><code>.wg-</code></td>
      <td><code>.wg-sm-</code></td>
      <td><code>.wg-md-</code></td>
      <td><code>.wg-lg-</code></td>
      <td><code>.wg-xl-</code></td>
    </tr>
    <tr>
      <th class="text-nowrap" scope="row"># of columns</th>
      <td colspan="5">12</td>
    </tr>
    <tr>
      <th class="text-nowrap" scope="row">Gutter width</th>
      <td colspan="5">30px (15px on each side of a column)</td>
    </tr>
    <tr>
      <th class="text-nowrap" scope="row">Offsets</th>
      <td colspan="5">No</td>
    </tr>
    <tr>
      <th class="text-nowrap" scope="row">Column ordering</th>
      <td colspan="5">No</td>
    </tr>
  </tbody>
</table>

Grid widget menggunakan `margin-left` dan `margin-right` untuk membuat *gutters*/jarak antara widget, dan menggunakan `calc()` untuk mengkalkulasi lebar dan jarak widget. Menggunakan *margin* dan `calc()` adalah untuk menghindari penggunaan `padding` pada `.widget`, agar tidak terjadi konflik dengan CSS widget lainnya.

### Examples

<div class="bd-example bd-example-widget-inverse text-white">
  <div class="wg wg-title-white wg-sm-6 wg-md-4 wg-lg-3 wg-grid-example">
    <div class="widget">
      <h4 class="title">Widget title</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
    <div class="widget">
      <h4 class="title">Widget title</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
    <div class="widget">
      <h4 class="title">Widget title</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
    <div class="widget">
      <h4 class="title">Widget title</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
</div><!-- /.bd-example -->

{% highlight html %}
<b:section class='wg wg-title-white wg-sm-6 wg-md-4 wg-lg-3' id='sectionId'></b:section>
{% endhighlight %}

<div class="bd-example">
  <div class="wg wg-box wg-box-orange wg-title-black wg-sm-6 wg-md-4 wg-grid-example">
    <div class="widget">
      <h4 class="title">Widget title</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
    <div class="widget">
      <h4 class="title">Widget title</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
    <div class="widget">
      <h4 class="title">Widget title</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
    <div class="widget">
      <h4 class="title">Widget title</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
</div><!-- /.bd-example -->

{% highlight html %}
<b:section class='wg wg-box wg-box-orange wg-title-black wg-sm-6 wg-md-4' id='sectionId'></b:section>
{% endhighlight %}

<div class="bd-example">
  <div class="wg wg-panel wg-panel-orange wg-title-black wg-sm-6 wg-grid-example">
    <div class="widget">
      <h4 class="title">Widget title</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
    <div class="widget">
      <h4 class="title">Widget title</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
    <div class="widget">
      <h4 class="title">Widget title</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
    <div class="widget">
      <h4 class="title">Widget title</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
</div><!-- /.bd-example -->

{% highlight html %}
<b:section class='wg wg-panel wg-panel-orange wg-title-black wg-sm-6' id='sectionId'></b:section>
{% endhighlight %}

### Equal height columns

Tambahkan `.wg-equal-height-cols` untuk membuat kolom sama tinggi.

<div class="bd-example">
  <div class="wg wg-box wg-box-orange wg-title-black wg-sm-6 wg-equal-height-cols wg-grid-example">
    <div class="widget">
      <h4 class="title">Widget title</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
    <div class="widget">
      <h4 class="title">Widget title</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
    <div class="widget">
      <h4 class="title">Widget title</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
    <div class="widget">
      <h4 class="title">Widget title</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
</div><!-- /.bd-example -->

{% highlight html %}
<b:section class='wg wg-box wg-box-orange wg-title-black wg-sm-6 wg-equal-height-cols' id='sectionId'></b:section>
{% endhighlight %}

<div class="bd-example">
  <div class="wg wg-panel wg-panel-orange wg-title-black wg-sm-6 wg-equal-height-cols wg-grid-example">
    <div class="widget">
      <h4 class="title">Widget title</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
    <div class="widget">
      <h4 class="title">Widget title</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
    <div class="widget">
      <h4 class="title">Widget title</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
    <div class="widget">
      <h4 class="title">Widget title</h4>
      <div class="widget-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      </div>
    </div><!-- /.widget -->
  </div>
</div><!-- /.bd-example -->

{% highlight html %}
<b:section class='wg wg-panel wg-panel-orange wg-title-black wg-sm-6 wg-equal-height-cols' id='sectionId'></b:section>
{% endhighlight %}

## `.wg-section-no-mb`

Gunakan `.wg-section-no-mb` untuk menghilangkan *margin* bawah pada widget baris terakhir.

<div class="bd-example">
  <div class="p-3 bg-light d-inline-block">
    <div class="wg wg-box wg-box-orange wg-title-black wg-section-no-mb">
      <div class="widget">
        <h4 class="title">Widget title</h4>
        <div class="widget-content">
          <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
        </div>
      </div><!-- /.widget -->
      <div class="widget">
        <h4 class="title">Widget title</h4>
        <div class="widget-content">
          <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
        </div>
      </div><!-- /.widget -->
    </div>
  </div>
</div><!-- /.bd-example -->

{% highlight html %}
<div class='p-3 bg-light'>
  <b:section class='wg wg-box wg-box-orange wg-title-black wg-section-no-mb' id='sectionId'></b:section>
</div>
{% endhighlight %}

Grup:

<div class="bd-example">
  <div class="p-3 bg-light d-inline-block">
    <div class="wg wg-panel wg-panel-group wg-panel-orange wg-title-black wg-section-no-mb">
      <div class="widget">
        <h4 class="title">Widget title</h4>
        <div class="widget-content">
          <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
        </div>
      </div><!-- /.widget -->
      <div class="widget">
        <h4 class="title">Widget title</h4>
        <div class="widget-content">
          <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
        </div>
      </div><!-- /.widget -->
    </div>
  </div>
</div><!-- /.bd-example -->

{% highlight html %}
<div class='p-3 bg-light'>
  <b:section class='wg wg-panel wg-panel-group wg-panel-orange wg-title-black wg-section-no-mb' id='sectionId'></b:section>
</div>
{% endhighlight %}

Dengan grid:

<div class="bd-example">
  <div class="p-3 bg-light">
    <div class="wg wg-panel wg-panel-orange wg-title-black wg-sm-6 wg-section-no-mb wg-grid-example">
      <div class="widget">
        <h4 class="title">Widget title</h4>
        <div class="widget-content">
          <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
        </div>
      </div><!-- /.widget -->
      <div class="widget">
        <h4 class="title">Widget title</h4>
        <div class="widget-content">
          <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
        </div>
      </div><!-- /.widget -->
      <div class="widget">
        <h4 class="title">Widget title</h4>
        <div class="widget-content">
          <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
        </div>
      </div><!-- /.widget -->
      <div class="widget">
        <h4 class="title">Widget title</h4>
        <div class="widget-content">
          <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
        </div>
      </div><!-- /.widget -->
    </div>
  </div>
</div><!-- /.bd-example -->

{% highlight html %}
<div class='p-3 bg-light'>
  <b:section class='wg wg-panel wg-panel-orange wg-title-black wg-sm-6 wg-section-no-mb' id='sectionId'></b:section>
</div>
{% endhighlight %}
