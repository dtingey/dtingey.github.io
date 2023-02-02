---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: "Home"
permalink: /
---

<h1>{{ page.title }}</h1>

<ul>
{% for post in site.posts %}
  <li>
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
    <p>{{ post.excerpt }}</p>
  </li>
{% endfor %}
</ul>


This is Damon Tingey. I like to eat chicken. [About](https://dtingey.github.io/about/)
