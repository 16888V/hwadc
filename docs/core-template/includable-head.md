---
layout: docs
title: Includable - Head
description: Tag title, tag meta, tag link, dan lainnya.
group: core-template
toc: true
---

## Required meta tags

- Set charset dengan `utf-8`.
- Gunakan tag meta responsif `viewport`.

###### Source

{% highlight plaintext %}
template-src/includable/head/head.requiredMetaTags.xml
{% endhighlight %}

###### Includable

{% highlight html %}
<b:includable id='head.requiredMetaTags'>...</b:includable>
{% endhighlight %}

###### Usage

{% highlight html %}
<b:include name='head.requiredMetaTags'/>
{% endhighlight %}

## All-head-content

Custom `<b:include data='blog' name='all-head-content'/>`.

###### Source

{% highlight plaintext %}
template-src/includable/head/head.allHeadContent.xml
{% endhighlight %}

###### Includable

{% highlight html %}
<b:includable id='head.allHeadContent'>...</b:includable>
{% endhighlight %}

###### Usage

{% highlight html %}
<b:include name='head.allHeadContent'/>
{% endhighlight %}

## Title

Judul dokumen atau tag `<title>`.

###### Source

{% highlight plaintext %}
template-src/includable/head/head.title.xml
{% endhighlight %}

###### Includable

{% highlight html %}
<b:includable id='head.title'>...</b:includable>
{% endhighlight %}

###### Usage

{% highlight html %}
<b:include name='head.title'/>
{% endhighlight %}

## SERP and social tags

Tag `<meta>` dan `<link>` untuk <abbr title="Search Engine Results Page">SERP</abbr> dan jejaring sosial.
###### Source

{% highlight plaintext %}
- Default/SERP: template-src/includable/head/head.defaultTags.xml
- Facebook Open Graph: template-src/includable/head/head.facebookTags.xml
- Twitter Cards: template-src/includable/head/head.twitterTags.xml
{% endhighlight %}

###### Includable

{% highlight html %}
<!-- Default/SERP -->
<b:includable id='head.defaultTags'>...</b:includable>
<!-- Facebook Open Graph -->
<b:includable id='head.facebookTags'>...</b:includable>
<!-- Twitter Cards -->
<b:includable id='head.twitterTags'>...</b:includable>
{% endhighlight %}

###### Usage

{% highlight html %}
<b:with value='"https://example.com/path/to/image.png"' var='image'>
<b:with value='"@username_of_website"' var='twitterUsernameWebsite'>
<b:with value='"@username_of_content_creator"' var='twitterUsernameCreator'>
  <b:include name='head.defaultTags'/>
  <b:include name='head.facebookTags'/>
  <b:include name='head.twitterTags'/>
</b:with>
</b:with>
</b:with>
{% endhighlight %}

## Example usage

{% highlight html %}
<!DOCTYPE html>
<html>
  <head>
    
    <b:include name='head.requiredMetaTags'/>
    <b:include name='head.title'/>
    <b:include name='head.allHeadContent'/>

    <b:with value='"https://example.com/path/to/image.png"' var='image'>
    <b:with value='"@username_of_website"' var='twitterUsernameWebsite'>
    <b:with value='"@username_of_content_creator"' var='twitterUsernameCreator'>
      <b:include name='head.defaultTags'/>
      <b:include name='head.facebookTags'/>
      <b:include name='head.twitterTags'/>
    </b:with>
    </b:with>
    </b:with>

  </head>
  <body>

    <h1>Hello, world!</h1>
    
  </body>
</html>
{% endhighlight %}
