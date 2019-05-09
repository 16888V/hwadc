---
layout: docs
title: Post
description: Bagian-bagian template untuk mengatur tampilan posting blog.
group: core-template
toc: true
---

## Breadcrumb

Untuk menunjukkan lokasi halaman saat ini.

###### Source

{% highlight plaintext %}
template-src/post/blog-breadcrumb.xml
{% endhighlight %}

###### Includable

{% highlight html %}
<b:includable id='blog-breadcrumb' var='post'>...</b:includable>
{% endhighlight %}

###### Usage

{% highlight html %}
<b:include cond='!data:view.isHomepage' name='blog-breadcrumb'/>
{% endhighlight %}

## Status message

Pesan yang akan muncul di atas posting. Pesan hanya akan muncul di halaman hasil pencarian, halaman label, halaman arsip, dan halaman galat (404).

###### Source

{% highlight plaintext %}
template-src/post/blog-status-message.xml
{% endhighlight %}

###### Includable

{% highlight html %}
<b:includable id='blog-status-message' var='post'>...</b:includable>
{% endhighlight %}

###### Usage

{% highlight html %}
<b:include name='blog-status-message'/>
{% endhighlight %}

## Posts

Posting dibagi menjadi beberapa bagian berdasarkan tipe halaman, untuk membuat tampilan posting yang berbeda di setiap tipe halaman, Anda hanya perlu menyesuaikan tampilan posting pada masing-masing bagian.

Dalam membuat tampilan posting, Anda membutuhkan penggunaan [includable untuk posting blog]({{ site.baseurl }}/core-template/includable-post/).

###### Source

{% highlight plaintext %}
template-src/post/blog-posts.xml
{% endhighlight %}

###### Includable

{% highlight html %}
<b:includable id='blog-posts' var='post'>...</b:includable>
{% endhighlight %}

###### Usage

{% highlight html %}
<b:include cond='data:posts.notEmpty' name='blog-posts'/>
{% endhighlight %}

## Comments

Sistem komentar bawaan Bootsblogger menggunakan **Google+ comments**.

###### Source

{% highlight plaintext %}
template-src/post/blog-comments.xml
{% endhighlight %}

###### Includable

{% highlight html %}
<b:includable id='blog-comments' var='post'>...</b:includable>
{% endhighlight %}

###### Usage

{% highlight html %}
<b:include cond='data:view.isPost' name='blog-comments'/>
{% endhighlight %}

## Pager

Tautan untuk menuju halaman berikutnya atau sebelumnya.

###### Source

{% highlight plaintext %}
template-src/post/blog-pager.xml
{% endhighlight %}

###### Includable

{% highlight html %}
<b:includable id='blog-pager' var='post'>...</b:includable>
{% endhighlight %}

###### Usage

{% highlight html %}
<b:include cond='data:posts.notEmpty and !data:view.isPage' name='blog-pager'/>
{% endhighlight %}

## Usage

Lihat `template-src/widgets/b-section-main__Blog1.xml`:

{% highlight html %}
<b:widget id='Blog1' locked='true' title='Blog Posts' type='Blog' version='2' visible='true'>
  <b:includable id='main'>

    <b:comment>=== Breadcrumb ===</b:comment>
    <b:include cond='!data:view.isHomepage' name='blog-breadcrumb'/>

    <b:comment>=== Status message ===</b:comment>
    <b:include name='blog-status-message'/>

    <b:comment>=== Posts ===</b:comment>
    <b:include cond='data:posts.notEmpty' name='blog-posts'/>

    <b:comment>=== Comments ===</b:comment>
    <b:include cond='data:view.isPost' name='blog-comments'/>

    <b:comment>=== Pager ===</b:comment>
    <b:include cond='data:posts.notEmpty and !data:view.isPage' name='blog-pager'/>

  </b:includable>
</b:widget>
{% endhighlight %}
