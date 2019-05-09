---
layout: docs
title: Overview
description: Template dasar Bootsblogger dirancang untuk memberikan kemudahan dengan mengubahsuaikan fitur bawaan Blogger dan menambahkan fitur-fitur baru.
group: core-template
redirect_from: "/core-template/"
toc: true
---

## Blogger version

Menggunakan template versi `3`:

{% highlight html %}
<html b:layoutsVersion='3'>...</html>
{% endhighlight %}

Menggunakan gadget versi `2`:

{% highlight html %}
<html b:defaultwidgetversion='2'>...</html>
{% endhighlight %}

{% highlight html %}
<b:widget version='2'>...</b:widget>
{% endhighlight %}

## Page types

Anda dapat mengatur tampilan blog, tampilan posting, kelas, dan lainnya menjadi berbeda di setiap tipe halaman.

Di bawah ini adalah seleksi tipe halaman menggunakan `data:view`.

{% highlight html %}
<b:comment>=== Homepage ===</b:comment>
<b:if cond='data:view.isHomepage'>
  <!-- https://example.blogspot.com -->
</b:if>

<b:comment>=== Item page ===</b:comment>
<b:if cond='data:view.isPost'>
  <!-- https://example.blogspot.com/<year>/<month>/<permalink>.html -->
</b:if>

<b:comment>=== Static page ===</b:comment>
<b:if cond='data:view.isPage'>
  <!-- https://example.blogspot.com/p/<permalink>.html -->
</b:if>

<b:comment>=== Search (label) page ===</b:comment>
<b:if cond='data:view.search.label'>
  <!-- https://example.blogspot.com/search/label/<name> -->
</b:if>

<b:comment>=== Search (query) page ===</b:comment>
<b:if cond='data:view.search.query'>
  <!-- https://example.blogspot.com/search?q=<query> -->
</b:if>

<b:comment>=== Search (default) page ===</b:comment>
<b:if cond='data:view.search and !data:view.search.label and !data:view.search.query'>
  <!-- https://example.blogspot.com/search -->
</b:if>

<b:comment>=== Archive page ===</b:comment>
<b:if cond='data:view.isArchive'>
  <!-- 1. https://example.blogspot.com/<year> -->
  <!-- 2. https://example.blogspot.com/<year>/<month> -->
  <!-- 3. https://example.blogspot.com/<year>_<month>_<day>_archive.html -->
</b:if>

<b:comment>=== Error page ===</b:comment>
<b:if cond='data:view.isError'>
  <!-- https://example.blogspot.com/404 -->
</b:if>

<b:comment>=== Preview page ===</b:comment>
<b:if cond='data:view.isPreview'>
  <!-- Preview page -->
</b:if>

<b:comment>=== Layout mode ===</b:comment>
<b:if cond='data:view.isLayoutMode'>
  <!-- https://www.blogger.com/blogger.g?blogID=<blogID>#pageelements -->
</b:if>
{% endhighlight %}

## Body class

Pada tag body HTML, terdapat kelas yang berbeda di setiap tipe halaman.

Di bawah ini adalah nama kelas tiap-tiap tipe halaman.

{% highlight html %}
<body>
  <b:class cond='data:view.isHomepage' name='blog-view-home'/>
  <b:class cond='data:view.isPost' name='blog-view-item'/>
  <b:class cond='data:view.isPage' name='blog-view-static'/>
  <b:class cond='data:view.search.label' name='blog-view-search-label'/>
  <b:class cond='data:view.search.query' name='blog-view-search-query'/>
  <b:class cond='data:view.search and !data:view.search.label and !data:view.search.query' name='blog-view-search-default'/>
  <b:class cond='data:view.isArchive' name='blog-view-archive'/>
  <b:class cond='data:view.isError' name='blog-view-error'/>
  <b:class cond='data:view.isPreview' name='blog-view-preview'/>
</body>
{% endhighlight %}

{% highlight html %}
<!-- Homepage -->
<body class="blog-view-home">...</body>

<!-- Item page -->
<body class="blog-view-item">...</body>

<!-- Static page -->
<body class="blog-view-static">...</body>

<!-- Search (label) page -->
<body class="blog-view-search-label">...</body>

<!-- Search (query) page -->
<body class="blog-view-search-query">...</body>

<!-- Search (default) page -->
<body class="blog-view-search-default">...</body>

<!-- Archive page -->
<body class="blog-view-archive">...</body>

<!-- Error page -->
<body class="blog-view-error">...</body>

<!-- Preview page -->
<body class="blog-view-preview">...</body>
{% endhighlight %}

Contoh pemanfaatan:

{% highlight css %}
.blog-view-item {
  ...
}

.blog-view-item .element {
  ...
}
{% endhighlight %}
