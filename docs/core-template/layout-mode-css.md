---
layout: docs
title: Layout mode CSS
description: CSS untuk halaman tata letak Blogger.
group: core-template
---

Untuk lebih jelas <a href="#" data-toggle="modal" data-target="#modalImgBloggerLayout">lihat gambar ini</a>.

## Source

Lihat `template-src/layout-mode.css`:

{% highlight css %}
/* Clearfix */
body#layout .container::after,
body#layout .section::after {
  display: block;
  content: "";
  clear: both;
}

/* Container */
body#layout .container {
  max-width: 100%;
}

/* Grid */
body#layout .blogger-col-1,
body#layout .blogger-col-2,
body#layout .blogger-col-3,
body#layout .blogger-col-4,
body#layout .blogger-col-5,
body#layout .blogger-col-6,
body#layout .blogger-col-7,
body#layout .blogger-col-8,
body#layout .blogger-col-9,
body#layout .blogger-col-10,
body#layout .blogger-col-11,
body#layout .blogger-col-12 {
  position: relative;
  float: left;
}
body#layout .blogger-col-1 {
  width: 8.33333333%;
}
body#layout .blogger-col-2 {
  width: 16.66666667%;
}
body#layout .blogger-col-3 {
  width: 25%;
}
body#layout .blogger-col-4 {
  width: 33.33333333%;
}
body#layout .blogger-col-5 {
  width: 41.66666667%;
}
body#layout .blogger-col-6 {
  width: 50%;
}
body#layout .blogger-col-7 {
  width: 58.33333333%;
}
body#layout .blogger-col-8 {
  width: 66.66666667%;
}
body#layout .blogger-col-9 {
  width: 75%;
}
body#layout .blogger-col-10 {
  width: 83.33333333%;
}
body#layout .blogger-col-11 {
  width: 91.66666667%;
}
body#layout .blogger-col-12 {
  width: 100%;
}

/* Lists */
body#layout ul,
body#layout ol {
  padding-left: 0;
  list-style: none;
}

/* Navbar */
body#layout .navbar {
  max-width: 500px;
  margin-right: auto;
  margin-left: auto;
}
{% endhighlight %}

### Grid usage

Gunakan pada elemen yang di dalamnya terdapat tag `b:section`. Sesuaikan dengan kerangka template.

<table class="table table-bordered table-striped table-responsive">
  <tbody>
    <tr>
      <th class="text-nowrap" scope="row">Grid behavior</th>
      <td>Horizontal at all times</td>
    </tr>
    <tr>
      <th class="text-nowrap" scope="row">Class prefix</th>
      <td><code>.blogger-col-</code></td>
    </tr>
    <tr>
      <th class="text-nowrap" scope="row"># of columns</th>
      <td>12</td>
    </tr>
  </tbody>
</table>

{% highlight html %}
<div class='container'>
  <!-- Main -->
  <main class='main blogger-col-8' id='main'>
    <b:section id='b-section-main' maxwidgets='1' name='Main' showaddelement='no'></b:section>
  </main><!-- /.main -->

  <!-- Sidebar -->
  <aside class='sidebar blogger-col-4' id='sidebar'>
    <b:section id='b-section-sidebar' name='Sidebar'></section>
  </aside><!-- /.sidebar -->
</div>
{% endhighlight %}

Hasilnya akan seperti pada <a href="#" data-toggle="modal" data-target="#modalImgBloggerLayoutGridExample">gambar ini</a>.

Dengan grid Bootstrap:

{% highlight html %}
<div class='container'>
  <div class='row'>
    <!-- Main -->
    <main class='col-md-8 col-lg-9 main blogger-col-8' id='main'>
      <b:section id='b-section-main' maxwidgets='1' name='Main' showaddelement='no'></b:section>
    </main><!-- /.main -->

    <!-- Sidebar -->
    <aside class='col-md-4 col-lg-3 sidebar blogger-col-4' id='sidebar'>
      <b:section id='b-section-sidebar' name='Sidebar'></section>
    </aside><!-- /.sidebar -->
  </div><!-- /.row -->
</div><!-- /.container -->
{% endhighlight %}
