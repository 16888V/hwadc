---
layout: docs
title: Head
description: Penjelasan bagian-bagian yang ada di dalam `<head>`.
group: core-template
---

Berikut ini adalah bagian-bagian yang ada di dalam `<head>`.

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc}

## Custom all-head-content <small class="text-muted">custom-all-head-content.xml</small>

Tag `<meta>` dan `<link>`—bawaan Blogger—tersuai.

Bawaan:

{% highlight html %}
<b:include data='blog' name='all-head-content'/>
{% endhighlight %}

Tersuai:

{% highlight html %}
<meta content='blogger' name='generator'/>

<link expr:href='data:blog.homepageUrl + &quot;favicon.ico&quot;' rel='icon'/>

<link expr:href='data:blog.homepageUrl + &quot;feeds/posts/default&quot;' expr:title='data:blog.title + &quot; » Atom&quot;' rel='alternate' type='application/atom+xml'/>

<link expr:href='data:blog.homepageUrl + &quot;feeds/comments/default&quot;' expr:title='data:blog.title + &quot; » Comments Feed&quot;' rel='alternate' type='application/atom+xml'/>

<b:if cond='data:blog.pageType == &quot;item&quot;'>
  <link expr:href='data:blog.homepageUrl + &quot;feeds/&quot; + data:blog.postId + &quot;/comments/default&quot;' expr:title='data:blog.title + &quot; » &quot; + data:blog.pageName + &quot; Comments Feed&quot;' rel='alternate' type='application/atom+xml'/>
</b:if>

<b:if cond='data:blog.searchLabel'>
  <link expr:href='data:blog.homepageUrl + &quot;feeds/posts/default/-/&quot; + data:blog.pageName' expr:title='data:blog.title + &quot; » &quot; + data:blog.pageName' rel='alternate' type='application/atom+xml'/>
</b:if>

<b:if cond='data:blog.pageType not in [&quot;item&quot;, &quot;static_page&quot;, &quot;archive&quot;]'>
  <link href='https://www.blogger.com/openid-server.g' rel='openid.server'/>
  <link expr:href='data:blog.homepageUrl' rel='openid.delegate'/>
</b:if>
{% endhighlight %}

Pengubahsuaian ini untuk validasi dan penambahan *feeds* untuk komentar dan label.

## Title <small class="text-muted">title.xml</small>

Tag `<title>` tersuai.

Bawaan:

{% highlight html %}
<title><data:blog.pageTitle/></title>
{% endhighlight %}

Tersuai:

{% highlight html %}
<b:if cond='data:blog.pageType == &quot;item&quot;'>
  <!-- Item/single page -->
  <title><data:blog.pageName/> | <data:blog.title/></title>

<b:elseif cond='data:blog.pageType == &quot;static_page&quot;'/>
  <!-- Static page -->
  <title><data:blog.pageName/> | <data:blog.title/></title>

<b:elseif cond='data:blog.searchLabel'/>
  <!-- Label/category page -->
  <title><data:blog.pageName/> | <data:blog.title/></title>

<b:elseif cond='data:blog.searchQuery'/>
  <!-- Search results page -->
  <title>Search Results for -<data:blog.searchQuery/>- | <data:blog.title/></title>

<b:elseif cond='data:blog.pageType == &quot;archive&quot;'/>
  <!-- Archive page -->
  <title>Archive for <data:blog.pageName/> | <data:blog.title/></title>

<b:elseif cond='data:blog.pageType == &quot;error_page&quot;'/>
  <!-- Error page -->
  <title>Page Not Found</title>

<b:else/>
  <!-- Homepage and default (https://example.blogspot.com/search) -->
  <title><data:blog.title/></title>
</b:if>
{% endhighlight %}

Dengan pengubahsuaian ini Anda dapat menampilkan judul dengan gaya sesuai yang Anda inginkan.

## Meta and link tags

Tag `<meta>` adalah elemen HTML yang digunakan untuk membentuk struktur metadata dari sebuah halaman web/blog. [Metadata](http://w3schools.com/tags/tag_meta.asp) adalah data (informasi) tentang data atau data informasi tentang berbagai aspek dari blog, seperti judul, deskripsi, gambar, URL, dan lain-lain.

### Required meta tags <small class="text-muted">meta-tags-required.xml</small>

- Set charset dengan `utf-8`.
- Gunakan tag meta responsif `viewport`.

{% highlight html %}
<meta charset='utf-8'/>
<meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
{% endhighlight %}

### Default <small class="text-muted">meta-tags-default.xml</small>

Tag `<meta>` dan `<link>` standar.

{% highlight html %}
<b:if cond='data:blog.pageType != &quot;error_page&quot;'>
  <link expr:href='data:blog.canonicalUrl' rel='canonical'/>
</b:if>
<b:if cond='data:blog.pageType == &quot;error_page&quot;'>
  <link expr:href='data:blog.homepageUrl + &quot;404&quot;' rel='canonical'/>
</b:if>

<b:if cond='data:blog.pageType == &quot;item&quot;'>
  <!-- Item/single page -->
  <b:if cond='data:blog.metaDescription'>
    <meta expr:content='data:blog.metaDescription' name='description'/>
  <b:else/>
    <meta expr:content='data:blog.pageName' name='description'/>
  </b:if>
  <b:if cond='data:blog.postImageUrl'><!-- Original size -->
    <link expr:href='data:blog.postImageUrl' rel='image_src'/>
  <b:elseif cond='data:blog.postImageThumbnailUrl'/><!-- 72 x 72 -->
    <link expr:href='data:blog.postThumbnailUrl' rel='image_src'/>
  <b:else/><!-- No image -->
    <link href='https://placehold.it/512/eee/png?text=NO+IMAGE+AVAILABLE' rel='image_src'/>
  </b:if>

<b:elseif cond='data:blog.pageType == &quot;static_page&quot;'/>
  <!-- Static page -->
  <b:if cond='data:blog.metaDescription'>
    <meta expr:content='data:blog.metaDescription' name='description'/>
  <b:else/>
    <meta expr:content='data:blog.pageName' name='description'/>
  </b:if>
  <link href='https://placehold.it/256/eee/png?text=Page' rel='image_src'/>

<b:elseif cond='data:blog.searchLabel'/>
  <!-- Label/category page -->
  <meta expr:content='{{ "{{ blog.meta.description.labelPage " }}}}' name='description'/>
  <link expr:href='&quot;https://placehold.it/512/eee/png?text=&quot; + data:blog.pageName' rel='image_src'/>

<b:elseif cond='data:blog.searchQuery'/>
  <!-- Search results page -->
  <meta expr:content='{{ "{{ blog.meta.description.searchResultsPage " }}}}' name='description'/>
  <link href='https://placehold.it/256/eee/png?text=Search' rel='image_src'/>

<b:elseif cond='data:blog.pageType == &quot;archive&quot;'/>
  <!-- Archive page -->
  <meta expr:content='{{ "{{ blog.meta.description.archivePage " }}}}' name='description'/>
  <link expr:href='&quot;https://placehold.it/512/eee/png?text=&quot; + data:blog.pageName' rel='image_src'/>

<b:elseif cond='data:blog.pageType == &quot;error_page&quot;'/>
  <!-- Error page -->
  <meta content='{{ "{{ blog.meta.description.errorPage " }}}}' name='description'/>
  <link href='https://placehold.it/256/eee/png?text=404' rel='image_src'/>

<b:else/>
  <!-- Homepage and default (https://example.blogspot.com/search) -->
  <b:if cond='data:blog.metaDescription'>
    <meta expr:content='data:blog.metaDescription' name='description'/>
  <b:else/>
    <meta content='{{ "{{ blog.meta.description.homePage " }}}}' name='description'/>
  </b:if>
  <meta content='{{ "{{ blog.meta.keywords " }}}}' name='keywords'/>
  <link href='{{ "{{ blog.social.image " }}}}' rel='image_src'/>
</b:if>
{% endhighlight %}

### Twitter Cards <small class="text-muted">meta-tags-twitter.xml</small>

Tag `<meta>` untuk jejaring sosial [Twitter](https://twitter.com).

{% highlight html %}
<b:if cond='data:blog.url == data:blog.homepageUrl'>
  <meta content='summary_large_image' name='twitter:card'/>
<b:else/>
  <meta content='summary' name='twitter:card'/>
</b:if>

<meta content='{{ "{{ social.twitterUsernameWebsite " }}}}' name='twitter:site'/>
<meta content='{{ "{{ social.twitterUsernameCreator " }}}}' name='twitter:creator'/>

<b:if cond='data:blog.pageType != &quot;error_page&quot;'>
  <meta expr:content='data:blog.canonicalUrl' name='twitter:url'/>
</b:if>
<b:if cond='data:blog.pageType == &quot;error_page&quot;'>
  <meta expr:content='data:blog.homepageUrl + &quot;404&quot;' name='twitter:url'/>
</b:if>

<b:if cond='data:blog.pageType == &quot;item&quot;'>
  <!-- Item/single page -->
  <meta expr:content='data:blog.pageName + &quot; | &quot; + data:blog.title' name='twitter:title'/>
  <b:if cond='data:blog.metaDescription'>
    <meta expr:content='data:blog.metaDescription' name='twitter:description'/>
  <b:else/>
    <meta expr:content='data:blog.pageName' name='twitter:description'/>
  </b:if>
  <b:if cond='data:blog.postImageUrl'><!-- Original size -->
    <meta expr:content='data:blog.postImageUrl' property='twitter:image'/>
  <b:elseif cond='data:blog.postImageThumbnailUrl'/><!-- 72 x 72 -->
    <meta expr:content='data:blog.postThumbnailUrl' property='twitter:image'/>
  <b:else/><!-- No image -->
    <meta content='https://placehold.it/512/eee/png?text=NO+IMAGE+AVAILABLE' property='twitter:image'/>
  </b:if>

<b:elseif cond='data:blog.pageType == &quot;static_page&quot;'/>
  <!-- Static page -->
  <meta expr:content='data:blog.pageName + &quot; | &quot; + data:blog.title' name='twitter:title'/>
  <b:if cond='data:blog.metaDescription'>
    <meta expr:content='data:blog.metaDescription' name='twitter:description'/>
  <b:else/>
    <meta expr:content='data:blog.pageName' name='twitter:description'/>
  </b:if>
  <meta content='https://placehold.it/256/eee/png?text=Page' property='twitter:image'/>

<b:elseif cond='data:blog.searchLabel'/>
  <!-- Label/category page -->
  <meta expr:content='{{ "{{ blog.meta.title.labelPage " }}}}' name='twitter:title'/>
  <meta expr:content='{{ "{{ blog.meta.description.labelPage " }}}}' name='twitter:description'/>
  <meta expr:content='&quot;https://placehold.it/512/eee/png?text=&quot; + data:blog.pageName' property='twitter:image'/>

<b:elseif cond='data:blog.searchQuery'/>
  <!-- Search results page -->
  <meta expr:content='{{ "{{ blog.meta.title.searchResultsPage " }}}}' name='twitter:title'/>
  <meta expr:content='{{ "{{ blog.meta.description.searchResultsPage " }}}}' name='twitter:description'/>
  <meta content='https://placehold.it/256/eee/png?text=Search' property='twitter:image'/>

<b:elseif cond='data:blog.pageType == &quot;archive&quot;'/>
  <!-- Archive page -->
  <meta expr:content='{{ "{{ blog.meta.title.archivePage " }}}}' name='twitter:title'/>
  <meta expr:content='{{ "{{ blog.meta.description.archivePage " }}}}' name='twitter:description'/>
  <meta expr:content='&quot;https://placehold.it/512/eee/png?text=&quot; + data:blog.pageName' property='twitter:image'/>

<b:elseif cond='data:blog.pageType == &quot;error_page&quot;'/>
  <!-- Error page -->
  <meta content='{{ "{{ blog.meta.title.errorPage " }}}}' name='twitter:title'/>
  <meta content='{{ "{{ blog.meta.description.errorPage " }}}}' name='twitter:description'/>
  <meta content='https://placehold.it/256/eee/png?text=404' property='twitter:image'/>

<b:else/>
  <!-- Homepage and default (https://example.blogspot.com/search) -->
  <meta expr:content='{{ "{{ blog.meta.title.homePage " }}}}' name='twitter:title'/>
  <b:if cond='data:blog.metaDescription'>
    <meta expr:content='data:blog.metaDescription' name='twitter:description'/>
  <b:else/>
    <meta content='{{ "{{ blog.meta.description.homePage " }}}}' name='twitter:description'/>
  </b:if>
  <meta content='{{ "{{ blog.social.image " }}}}' property='twitter:image'/>
</b:if>
{% endhighlight %}

### Facebook Open Graph <small class="text-muted">meta-tags-facebook.xml</small>

Tag `<meta>` untuk jejaring sosial [Facebook](https://facebook.com).

{% highlight html %}
<b:if cond='data:blog.pageType in [&quot;item&quot;, &quot;static_page&quot;]'>
  <meta content='article' property='og:type'/>
<b:else/>
  <meta content='website' property='og:type'/>
</b:if>

<meta expr:content='data:blog.title' property='og:site_name'/>

<b:if cond='data:blog.pageType != &quot;error_page&quot;'>
  <meta expr:content='data:blog.canonicalUrl' property='og:url'/>
</b:if>
<b:if cond='data:blog.pageType == &quot;error_page&quot;'>
  <meta expr:content='data:blog.homepageUrl + &quot;404&quot;' property='og:url'/>
</b:if>

<b:if cond='data:blog.pageType == &quot;item&quot;'>
  <!-- Item/single page -->
  <meta expr:content='data:blog.pageName + &quot; | &quot; + data:blog.title' property='og:title'/>
  <b:if cond='data:blog.metaDescription'>
    <meta expr:content='data:blog.metaDescription' property='og:description'/>
  <b:else/>
    <meta expr:content='data:blog.pageName' property='og:description'/>
  </b:if>
  <b:if cond='data:blog.postImageUrl'><!-- Original size -->
    <meta expr:content='data:blog.postImageUrl' property='og:image'/>
  <b:elseif cond='data:blog.postImageThumbnailUrl'/><!-- 72 x 72 -->
    <meta expr:content='data:blog.postThumbnailUrl' property='og:image'/>
  <b:else/><!-- No image -->
    <meta content='https://placehold.it/512/eee/png?text=NO+IMAGE+AVAILABLE' property='og:image'/>
  </b:if>

<b:elseif cond='data:blog.pageType == &quot;static_page&quot;'/>
  <!-- Static page -->
  <meta expr:content='data:blog.pageName + &quot; | &quot; + data:blog.title' property='og:title'/>
  <b:if cond='data:blog.metaDescription'>
    <meta expr:content='data:blog.metaDescription' property='og:description'/>
  <b:else/>
    <meta expr:content='data:blog.pageName' property='og:description'/>
  </b:if>
  <meta content='https://placehold.it/256/eee/png?text=Page' property='og:image'/>

<b:elseif cond='data:blog.searchLabel'/>
  <!-- Label/category page -->
  <meta expr:content='{{ "{{ blog.meta.title.labelPage " }}}}' property='og:title'/>
  <meta expr:content='{{ "{{ blog.meta.description.labelPage " }}}}' property='og:description'/>
  <meta expr:content='&quot;https://placehold.it/512/eee/png?text=&quot; + data:blog.pageName' property='og:image'/>

<b:elseif cond='data:blog.searchQuery'/>
  <!-- Search results page -->
  <meta expr:content='{{ "{{ blog.meta.title.searchResultsPage " }}}}' property='og:title'/>
  <meta expr:content='{{ "{{ blog.meta.description.searchResultsPage " }}}}' property='og:description'/>
  <meta content='https://placehold.it/256/eee/png?text=Search' property='og:image'/>

<b:elseif cond='data:blog.pageType == &quot;archive&quot;'/>
  <!-- Archive page -->
  <meta expr:content='{{ "{{ blog.meta.title.archivePage " }}}}' property='og:title'/>
  <meta expr:content='{{ "{{ blog.meta.description.archivePage " }}}}' property='og:description'/>
  <meta expr:content='&quot;https://placehold.it/512/eee/png?text=&quot; + data:blog.pageName' property='og:image'/>

<b:elseif cond='data:blog.pageType == &quot;error_page&quot;'/>
  <!-- Error page -->
  <meta content='{{ "{{ blog.meta.title.errorPage " }}}}' property='og:title'/>
  <meta content='{{ "{{ blog.meta.description.errorPage " }}}}' property='og:description'/>
  <meta content='https://placehold.it/256/eee/png?text=404' property='og:image'/>

<b:else/>
  <!-- Homepage and default (https://example.blogspot.com/search) -->
  <meta expr:content='{{ "{{ blog.meta.title.homePage " }}}}' property='og:title'/>
  <b:if cond='data:blog.metaDescription'>
    <meta expr:content='data:blog.metaDescription' property='og:description'/>
  <b:else/>
    <meta content='{{ "{{ blog.meta.description.homePage " }}}}' property='og:description'/>
  </b:if>
  <meta content='{{ "{{ blog.social.image " }}}}' property='og:image'/>
</b:if>
{% endhighlight %}

## Remove Blogger's default CSS <small class="text-muted">blogger-css-hack.xml</small>

Blogger memiliki bundel CSS yang digunakan untuk widget, gadget, dan juga elemen umum, seperti `html`, `body`, `h*`, `p`, dan lain-lain. Oleh karena itu, bundel CSS tersebut harus dihilangkan untuk menghindari konflik dengan CSS Bootstrap dan Bootsblogger.

Bundel CSS tersebut dihilangkan dengan kode di bawah ini:

{% highlight html %}
&lt;style&gt;
&lt;!--/*<b:skin><![CDATA[

*/]]></b:skin>
{% endhighlight %}

Kode di atas akan membuat bundel CSS Blogger berada di dalam komentar HTML, sehingga bundel CSS tersebut akan dianggap oleh *browser* hanya sebagai sebuah komentar HTML, bukan eksternal CSS.

## Grid system for Blogger <small class="text-muted">blogger-css-hack.xml</small>

Pada tulisan di atas, kita sudah membahas tentang menghilangkan bundel CSS Blogger. Selanjutnya kita akan membahas **sistem grid untuk tata letak widget** pada *dashboard* Blogger, <a href="javascript:;" data-toggle="modal" data-target=".image-blogger-layout">lihat gambar</a>. CSS sistem grid ini harus diletakan di dalam kode yang di atas tadi, seperti berikut:

**Catatan:** CSS ini hanya bekerja pada *dashboard* Blogger.

{% highlight html %}
&lt;style&gt;
&lt;!--/*<b:skin><![CDATA[

ul, ol { display: none; }

.blogger-col-1,
.blogger-col-2,
.blogger-col-3,
.blogger-col-4,
.blogger-col-5,
.blogger-col-6,
.blogger-col-7,
.blogger-col-8,
.blogger-col-9,
.blogger-col-10,
.blogger-col-11,
.blogger-col-12 {
  float: left;
}
.blogger-col-1 {
  width: 8.33333333%;
}
.blogger-col-2 {
  width: 16.66666667%;
}
.blogger-col-3 {
  width: 25%;
}
.blogger-col-4 {
  width: 33.33333333%;
}
.blogger-col-5 {
  width: 41.66666667%;
}
.blogger-col-6 {
  width: 50%;
}
.blogger-col-7 {
  width: 58.33333333%;
}
.blogger-col-8 {
  width: 66.66666667%;
}
.blogger-col-9 {
  width: 75%;
}
.blogger-col-10 {
  width: 83.33333333%;
}
.blogger-col-11 {
  width: 91.66666667%;
}
.blogger-col-12 {
  width: 100%;
}

*/]]></b:skin>
{% endhighlight %}

#### Usage

Gunakan pada elemen yang di dalamnya terdapat tag `b:section`. Sesuaikan dengan kerangka template.

{% highlight html %}
<div class='container'>
  <!-- Main -->
  <main class='main blogger-col-8' id='main'>
    <b:section class='' id='main-section' maxwidgets='1' showaddelement='no'></b:section>
  </main><!-- /.main -->

  <!-- Sidebar -->
  <aside class='sidebar blogger-col-4' id='sidebar'>
    <b:section class='' id='sidebar-section'></section>
  </aside><!-- /.sidebar -->
</div>
{% endhighlight %}

Hasilnya akan seperti pada <a href="javascript:;" data-toggle="modal" data-target=".image-blogger-layout">gambar ini</a>.

#### Notation

Jika Anda menggunakan sistem grid Bootstrap dan sistem grid untuk Blogger pada elemen yang sama, **kelas kolom tidak harus sama**, misal Anda menggunakan sistem grid Bootstrap untuk membuat template dua kolom dengan menggunakan `.col-md-9` untuk *main* dan `.col-md-3` untuk *sidebar*, penggunaan sistem grid untuk Blogger tidak harus menggunakan `.blogger-col-9` untuk *main* dan `.blogger-col-3` untuk *sidebar*, tetapi bisa juga `.blogger-col-8` untuk *main* dan `.blogger-col-4` untuk *sidebar*. Untuk lebih jelasnya lihat kode di bawah ini:

{% highlight html %}
<div class='container'>
  <div class='row'>
    <!-- Main -->
    <main class='main col-md-9 blogger-col-8' id='main'>
      <b:section class='' id='main-section' maxwidgets='1' showaddelement='no'></b:section>
    </main><!-- /.main -->

    <!-- Sidebar -->
    <aside class='sidebar col-md-3 blogger-col-4' id='sidebar'>
      <b:section class='' id='sidebar-section'></section>
    </aside><!-- /.sidebar -->
  </div><!-- /.row -->
</div><!-- /.container -->
{% endhighlight %}
