---

layout: default
title: Home
---

## 一篇文章

{% assign post0 = site.posts[0] %}

<hr class="slender">

### [{{ post.title }}]({{ post0.url | prepend: site.baseurl }}) <br>

{% marginnote "recent-posts" "近期文章：" %}

<span class="smaller">{{ post.date | date: "%B %-d, %Y" }}</span>  <br/>

{{ post.excerpt }}

<hr class="slender">

## 一张照片

{% fullwidth "assets/photo/sunset.jpg" "sunset" %}
