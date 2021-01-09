---
layout: page
show_meta: false
title: "Kubernets!"
subheadline: "1st Container Orchestration Tool"
header:
   image_fullwidth: "header_unsplash_5.jpg"
permalink: "/k8s/"
---
<ul>
    {% for post in site.categories.design %}
    <li><a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
</ul>