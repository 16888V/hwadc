---
layout: docs
title: Includable - Assets
description: CSS, JavaScript, icons, dan lainnya.
group: core-template
toc: true
---

## Required CSS

- Bootstrap
- Bootsblogger
- Font Awesome (CDN) - <http://fontawesome.io/>

###### Includable

{% highlight html %}
<b:includable id='assets.requiredCss'>...</b:includable>
{% endhighlight %}

###### Usage

{% highlight html %}
<b:include name='assets.requiredCss'/>
{% endhighlight %}

## Required JS

- jQuery (CDN) - <https://jquery.com/>
- Popper.js (CDN) - <https://popper.js.org/>
- Bootstrap

###### Includable

{% highlight html %}
<b:includable id='assets.requiredJs'>...</b:includable>
{% endhighlight %}

###### Usage

{% highlight html %}
<b:include name='assets.requiredJs'/>
{% endhighlight %}

## Icons

Inline SVG icons.

### Blogger

###### Source

{% highlight plaintext %}
template-src/includable/assets/icons/assets.bloggerIcon.xml
{% endhighlight %}

###### Includable

{% highlight html %}
<b:includable id='assets.bloggerIcon'>...</b:includable>
{% endhighlight %}

###### Usage

{% highlight html %}
<b:include data='{ width: number, height: number, fillBg: "#ff5722", fillB: "#fff", class: "class-name" }' name='assets.bloggerIcon'/>
{% endhighlight %}

**Example:**

<div class="bd-example">
  <svg class="align-middle" width="24" height="24" viewBox="0 0 612 612" xmlns="http://www.w3.org/2000/svg" focusable="false">
    <title>Blogger</title>
    <path fill="#ff5722" d="M612, 510c0, 56.1-45.9, 102-102, 102H102C45.9, 612, 0, 566.1, 0, 510V102C0, 45.9, 45.9, 0, 102, 0h408 c56.1, 0, 102, 45.9, 102, 102V510z"></path>
    <path fill="#fff" d="m 483.32742, 262.81768 c -7.88887, -3.44838 -41.73045, 0.38183 -51.13171, -8.29282 -6.63342, -6.25243 -7.05677, -17.56407 -9.6465, -32.65819 -4.33566, -25.27222 -6.14292, -30.99964 -10.65377, -40.95102 -16.41131, -35.46224 -55.75058, -65.82947 -91.48993, -65.82947 l -82.8361, 0 c -65.17519, 0 -118.42655, 54.35078 -118.42655, 120.6814 l 0, 140.71541 c 0, 66.2113 53.25136, 120.43083 118.42655, 120.43083 l 136.10207, 0 c 65.17226, 0 118.06159, -54.21953 118.43823, -120.43083 l 0.74743, -97.4615 c 0, 0 0, -12.05144 -9.52972, -16.20381 m -244.26024, -49.11258 65.67737, 0 c 12.5311, 0 22.68271, 10.33321 22.68271, 22.95738 0, 12.63611 -10.15161, 23.08864 -22.68271, 23.08864 l -65.67737, 0 c -12.53111, 0 -22.6827, -10.45253 -22.6827, -23.08864 0.003, -12.62417 10.15451, -22.95738 22.6827, -22.95738 m 133.47731, 183.9574 -133.47731, 0 c -12.53111, 0 -22.6827, -10.46447 -22.6827, -22.95739 0, -12.6361 10.15159, -22.96932 22.6827, -22.96932 l 133.47731, 0 c 12.40265, 0 22.55132, 10.33322 22.55132, 22.96932 0.003, 12.49292 -10.14867, 22.95739 -22.55132, 22.95739"></path>
  </svg>
  Blogger
</div>

{% highlight html %}
<b:include data='{ width: 24, height: 24, fillBg: "#ff5722", fillB: "#fff", class: "align-middle" }' name='assets.bloggerIcon'/> Blogger
{% endhighlight %}

## Example usage: CSS and JavaScript

{% highlight html %}
<!DOCTYPE html>
<html>
  <head>
    <b:include name='assets.requiredCss'/>
  </head>
  <body>
    <h1>Hello, world!</h1>

    <b:include name='assets.requiredJs'/>
  </body>
</html>
{% endhighlight %}
