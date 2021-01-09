---
layout: page
show_meta: false
title: "My Blog!"
subheadline: "How to build my blog"
header:
   image_fullwidth: "header_unsplash_5.jpg"
permalink: "/myblog/"
---
<ul>
    {% for post in site.categories.myblog %}
    <li><a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
</ul>