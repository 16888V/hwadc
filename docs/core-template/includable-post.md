---
layout: docs
title: Includable - Post
description: Includable untuk posting blog.
group: core-template
toc: true
---

## Post byline items

*Item* posting yang dapat diatur melalui konfigurasi posting blog (<a href="#" data-toggle="modal" data-target="#modalImgBloggerConfigureBlogPosts">lihat gambar</a>).

### Header

Untuk menampilkan *item* posting yang ada dalam kolom *header*.

###### Source

{% highlight plaintext %}
template-src/includable/post/post.header.xml
{% endhighlight %}

###### Includable

{% highlight html %}
<b:includable id='post.header'>...</b:includable>
{% endhighlight %}

###### Usage

{% highlight html %}
<b:if cond='data:headerByline.items.notEmpty'>
  <div class='wrapper'>
    <b:include name='post.header'/>
  </div>
</b:if>
{% endhighlight %}

### Footer

Untuk menampilkan *item* posting yang ada dalam kolom *footer*.

###### Source

{% highlight plaintext %}
template-src/includable/post/post.footer.xml
{% endhighlight %}

###### Includable

{% highlight html %}
<b:includable id='post.footer'>...</b:includable>
{% endhighlight %}

###### Usage

{% highlight html %}
<b:if cond='data:footerBylines.notEmpty'>
  <div class='wrapper'>
    <b:include name='post.footer'/>
  </div>
</b:if>
{% endhighlight %}

## Post items

*Item* posting di bawah ini tidak dapat diatur melalui konfigurasi posting blog.

### Title

Untuk menampilkan judul posting.

###### Source

{% highlight plaintext %}
template-src/includable/post/post.title.xml
{% endhighlight %}

###### Includable

{% highlight html %}
<b:includable id='post.title'>...</b:includable>
{% endhighlight %}

###### Usage

{% highlight html %}
<b:include data='{ heading: "h1|h2|h3|h4|h5|h6"|false, headingClass: "class-name", link: true|false, linkClass: "class-name", noTitleMessage: true|false }' name='post.title'/>
{% endhighlight %}

### Author name

Untuk menampilkan nama penulis.

###### Source

{% highlight plaintext %}
template-src/includable/post/post.authorName.xml
{% endhighlight %}

###### Includable

{% highlight html %}
<b:includable id='post.authorName'>...</b:includable>
{% endhighlight %}

###### Usage

{% highlight html %}
<b:include data='{ linkClass: "class-name" }' name='post.authorName'/>
{% endhighlight %}

### Author image

Untuk menampilkan foto penulis.

###### Source

{% highlight plaintext %}
template-src/includable/post/post.authorImage.xml
{% endhighlight %}

###### Includable

{% highlight html %}
<b:includable id='post.authorImage'>...</b:includable>
{% endhighlight %}

###### Usage

{% highlight html %}
<b:include data='{ size: number, ratioWidth: number, ratioHeight: number, noImage: "https://example.com/path/to/no-image.png"|false, imageClass: "class-name" }' name='post.authorImage'/>
{% endhighlight %}

**Example:**

Width = `size`, Height = ((`size` * `ratioHeight`) / `ratioWidth`).

128x128:

{% highlight html %}
<b:include data='{ size: 128, ratioWidth: 1, ratioHeight: 1, noImage: "https://placehold.it/128x128/777/eee/?text=NO+IMAGE", imageClass: "class-name" }' name='post.authorImage'/>
{% endhighlight %}

### Dates

Untuk menampilkan tanggal diterbitkannya posting dan tanggal terakhir posting diperbarui.

###### Source

{% highlight plaintext %}
- template-src/includable/post/post.datePublished.xml
- template-src/includable/post/post.dateUpdated.xml
{% endhighlight %}

###### Includable

{% highlight html %}
<b:includable id='post.datePublished'>...</b:includable>
<b:includable id='post.dateUpdated'>...</b:includable>
{% endhighlight %}

###### Usage

{% highlight html %}
Published: <b:include data='{ customFormat: "dd/MM/YYYY"|false, timeClass: "class-name" }' name='post.datePublished'/>
Last updated: <b:include data='{ customFormat: "dd/MM/YYYY"|false, timeClass: "class-name" }' name='post.dateUpdated'/>
{% endhighlight %}

**Format:**

<table class="table-responsive">
  <thead>
    <tr>
      <th>Period</th>
      <th>Symbol</th>
      <th>Example output</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="2">Year</td>
      <td><code>YY</code></td>
      <td><code>17</code></td>
      <td>Year, 2 digits</td>
    </tr>
    <tr>
      <td><code>YYYY</code></td>
      <td><code>2017</code></td>
      <td>Year, 4 digits</td>
    </tr>
    <tr>
      <td rowspan="5">Month</td>
      <td><code>M</code></td>
      <td><code>1</code>, <code>11</code></td>
      <td>Month, minimum 1 digit</td>
    </tr>
    <tr>
      <td><code>MM</code></td>
      <td><code>01</code>, <code>11</code></td>
      <td>Month, 2 digits</td>
    </tr>
    <tr>
      <td><code>MMM</code></td>
      <td><code>Jan</code>, <code>Nov</code></td>
      <td>Month, 3 Letters</td>
    </tr>
    <tr>
      <td><code>MMMM</code></td>
      <td><code>January</code>, <code>November</code></td>
      <td>Month, full name</td>
    </tr>
    <tr>
      <td><code>MMMMM</code></td>
      <td><code>J</code>, <code>N</code></td>
      <td>Month, 1st letter</td>
    </tr>
    <tr>
      <td rowspan="3">Week</td>
      <td><code>w</code></td>
      <td><code>1</code>, <code>11</code></td>
      <td>Week of the year, minimum 1 digit</td>
    </tr>
    <tr>
      <td><code>ww</code></td>
      <td><code>01</code>, <code>11</code></td>
      <td>Week of the year, 2 digits</td>
    </tr>
    <tr>
      <td><code>W</code></td>
      <td><code>4</code></td>
      <td>Week of the month, 1 digit</td>
    </tr>
    <tr>
      <td rowspan="10">Day</td>
      <td><code>d</code></td>
      <td><code>1</code>, <code>11</code></td>
      <td>Day of the month, minimum 1 digit</td>
    </tr>
    <tr>
      <td><code>dd</code></td>
      <td><code>01</code>, <code>11</code></td>
      <td>Day of the month, 2 digits</td>
    </tr>
    <tr>
      <td><code>D</code></td>
      <td><code>1</code>, <code>55</code>, <code>362</code></td>
      <td>Day of the year, minimum 1 digit</td>
    </tr>
    <tr>
      <td><code>DD</code></td>
      <td><code>01</code>, <code>55</code>, <code>362</code></td>
      <td>Day of the year, minimum 2 digits</td>
    </tr>
    <tr>
      <td><code>DDD</code></td>
      <td><code>001</code>, <code>055</code>, <code>362</code></td>
      <td>Day of the year, minimum 3 digits</td>
    </tr>
    <tr>
      <td><code>F</code></td>
      <td><code>3</code></td>
      <td>Xth day of the month. Example, the 3rd Tuesday of the month.</td>
    </tr>
    <tr>
      <td><code>E</code></td>
      <td><code>M</code>, <code>T</code></td>
      <td>Name of the day of the week. 1 letter</td>
    </tr>
    <tr>
      <td><code>EE</code></td>
      <td><code>Mo</code>, <code>Tu</code></td>
      <td>Name of the day of the week. 2 letters</td>
    </tr>
    <tr>
      <td><code>EEE</code></td>
      <td><code>Mon</code>, <code>Tue</code></td>
      <td>Name of the day of the week. 3 letters</td>
    </tr>
    <tr>
      <td><code>EEEE</code></td>
      <td><code>Monday</code>, <code>Tuesday</code></td>
      <td>Full name of the day of the week.</td>
    </tr>
    <tr>
      <td rowspan="3">Time of day</td>
      <td><code>aaaa</code></td>
      <td><code>AM</code>, <code>PM</code></td>
      <td rowspan="3">Names may vary depending on the region.</td>
    </tr>
    <tr>
      <td><code>bbbb</code></td>
      <td rowspan="2"><code>Morning</code>, <code>Afternoon</code>, <code>Evening</code></td>
    </tr>
    <tr>
      <td><code>BBBB</code></td>
    </tr>
    <tr>
      <td rowspan="4">Hour</td>
      <td><code>h</code></td>
      <td><code>1</code>, <code>11</code></td>
      <td>Time [1-12], minimum 1 digit</td>
    </tr>
    <tr>
      <td><code>hh</code></td>
      <td><code>01</code>, <code>11</code></td>
      <td>Time [1-12], 2 digits</td>
    </tr>
    <tr>
      <td><code>H</code></td>
      <td><code>1</code>, <code>21</code></td>
      <td>Time [0-23], minimum 1 digit</td>
    </tr>
    <tr>
      <td><code>HH</code></td>
      <td><code>01</code>, <code>21</code></td>
      <td>Time [0-23], 2 digits</td>
    </tr>
    <tr>
      <td rowspan="2">Minute</td>
      <td><code>m</code></td>
      <td><code>1</code>, <code>59</code></td>
      <td>Minute, minimum 1 digit</td>
    </tr>
    <tr>
      <td><code>mm</code></td>
      <td><code>01</code>, <code>59</code></td>
      <td>Minute, 2 digits</td>
    </tr>
  </tbody>
</table>

### Number of comments

Untuk menampilkan jumlah komentar per posting. Jika menggunakan sistem komentar Google+, yang tampil hanya `<data:messages.comments/>`.

###### Source

{% highlight plaintext %}
template-src/includable/post/post.numComments.xml
{% endhighlight %}

###### Includable

{% highlight html %}
<b:includable id='post.numComments'>...</b:includable>
{% endhighlight %}

###### Usage

{% highlight html %}
<b:if cond='data:post.allowComments'>
  <b:include data='{ linkClass: "class-name" }' name='post.numComments'/>
</b:if>
{% endhighlight %}

### Labels

Untuk menampilkan label posting.

###### Source

{% highlight plaintext %}
template-src/includable/post/post.labels.xml
{% endhighlight %}

###### Includable

{% highlight html %}
<b:includable id='post.labels'>...</b:includable>
{% endhighlight %}

###### Usage

{% highlight html %}
<b:include data='{ comma: true|false, maxResults: number, labelLinkClass: "class-name", unlabelledClass: "class-name" }' name='post.labels'/>
{% endhighlight %}

### Share

Untuk menampilkan tombol berbagi.

###### Source

{% highlight plaintext %}
template-src/includable/post/post.share.xml
{% endhighlight %}

###### Includable

{% highlight html %}
<b:includable id='post.share'>...</b:includable>
{% endhighlight %}

###### Usage

{% highlight html %}
<b:include data='{ parentDivClass: "dropdown|dropup|class-name", dropdownToggleLinkClass: "class-name", dropdownToggleType: "icon|text|all", dropdownMenuClass: "dropdown-menu", dropdownItemLinkClass: "dropdown-item", dropdownItemIcon: true|false }' name='post.share'/>
{% endhighlight %}

### Featured image

Untuk menampilkan *featured image*.

##### Using HTML `<img>`

###### Source

{% highlight plaintext %}
template-src/includable/post/post.featuredImage.xml
{% endhighlight %}

###### Includable

{% highlight html %}
<b:includable id='post.featuredImage'>...</b:includable>
{% endhighlight %}

###### Usage

{% highlight html %}
<b:include data='{ size: number, sourceSet: [number]|false, sourceSizes: "sizes"|false, ratioWidth: number, ratioHeight: number, link: true|false, noImage: "https://example.com/path/to/no-image.png"|false, imageClass: "class-name" }' name='post.featuredImage'/>
{% endhighlight %}

**Notation:**

Non-responsive: Width = `size`, Height = ((`size` * `ratioHeight`) / `ratioWidth`).

Responsive: Width = `sourceSet`, Height = ((`sourceSet` * `ratioHeight`) / `ratioWidth`).

**Example without `srcset` and `sizes`:**

{% highlight html %}
<b:include data='{ size: 512, sourceSet: false, sourceSizes: false, ratioWidth: 16, ratioHeight: 9, link: true, noImage: "https://placehold.it/512x288/777/eee/?text=NO+IMAGE", imageClass: "class-name" }' name='post.featuredImage'/>
{% endhighlight %}

**Example with `srcset`, but without `sizes`:**

{% highlight html %}
<!-- Example 1: `false` -->
<b:include data='{ size: 256, sourceSet: [256, 512, 1280, 1600], sourceSizes: false, ratioWidth: 16, ratioHeight: 9, link: true, noImage: "https://placehold.it/256x144/777/eee/?text=NO+IMAGE", imageClass: "class-name" }' name='post.featuredImage'/>

<!-- Example 2: `100vw` -->
<b:include data='{ size: 256, sourceSet: [256, 512, 1280, 1600], sourceSizes: "100vw", ratioWidth: 16, ratioHeight: 9, link: true, noImage: "https://placehold.it/256x144/777/eee/?text=NO+IMAGE", imageClass: "class-name" }' name='post.featuredImage'/>
{% endhighlight %}

**Example with `srcset` and `sizes`:**

{% highlight html %}
<b:include data='{ size: 256, sourceSet: [256, 512, 1280, 1600], sourceSizes: "(max-width: 575px) 256px, (max-width: 767px) 512px, (max-width: 991px) 1280px, 1600px", ratioWidth: 16, ratioHeight: 9, link: true, noImage: "https://placehold.it/256x144/777/eee/?text=NO+IMAGE", imageClass: "class-name" }' name='post.featuredImage'/>
{% endhighlight %}

##### Using CSS `background-image`

`post.featuredImageBg` tidak menggunakan `srcset` dan `sizes`.

###### Source

{% highlight plaintext %}
template-src/includable/post/post.featuredImageBg.xml
{% endhighlight %}

###### Includable

{% highlight html %}
<b:includable id='post.featuredImageBg'>...</b:includable>
{% endhighlight %}

###### Usage

{% highlight html %}
<div class='class-name'><!-- Target -->
  <b:include data='{ size: number, ratioWidth: number, ratioHeight: number, noImage: "https://example.com/path/to/no-image.png"|false, style: "min-height: <number><units>;" }' name='post.featuredImageBg'/>
</div>
{% endhighlight %}

**Example:**

Width = `size`, Height = ((`size` * `ratioHeight`) / `ratioWidth`).

{% highlight html %}
<div class='class-name'><!-- Target -->
  <b:include data='{ size: 512, ratioWidth: 16, ratioHeight: 9, noImage: "https://placehold.it/512x288/777/eee/?text=NO+IMAGE", style: "min-height: 288px;" }' name='post.featuredImageBg'/>
</div>
{% endhighlight %}

### Snippet

Untuk menampilkan ringkasan posting.

###### Source

{% highlight plaintext %}
template-src/includable/post/post.snippet.xml
{% endhighlight %}

###### Includable

{% highlight html %}
<b:includable id='post.snippet'>...</b:includable>
{% endhighlight %}

###### Usage

{% highlight html %}
<b:include data='{ length: number, links: true|false, linebreaks: true|false, ellipsis: true|false, notHasJumpLink: true|false, parentDivClass: "class-name" }' name='post.snippet'/>
{% endhighlight %}

Ketika posting menggunakan *jump break* dan `notHasJumpLink: true` maka yang ditampilkan adalah `<data:post.body/>`.

### Body

Sebagai pengganti `<data:post.body/>`.

###### Source

{% highlight plaintext %}
template-src/includable/post/post.body.xml
{% endhighlight %}

###### Includable

{% highlight html %}
<b:includable id='post.body'>...</b:includable>
{% endhighlight %}

###### Usage

{% highlight html %}
<b:include data='{ parentDivClass: "class-name" }' name='post.body'/>
{% endhighlight %}

### Jump link

Untuk menampilkan *jump link*.

###### Source

{% highlight plaintext %}
template-src/includable/post/post.jumpLink.xml
{% endhighlight %}

###### Includable

{% highlight html %}
<b:includable id='post.jumpLink'>...</b:includable>
{% endhighlight %}

###### Usage

{% highlight html %}
<b:include data='{ linkClass: "btn btn-primary", parentDivClass: "class-name" }' name='post.jumpLink'/>
{% endhighlight %}
