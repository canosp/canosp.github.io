---
layout: page
title: Projects
---

<img src="../assets/photos/f19-codesprint1.JPG" class="img-fluid" alt="Code Sprint - Fall 2019">

Industry mentors work with CANOSP students on various open-source projects
over the course of a semester. At the beginning of the term, students get to
rank the projects that they would like to work on and assigned to groups based
on their preferences. Here are some project proposals that CANOSP students got to
choose from:

## Current projects

{% for post in site.posts %}
{% if post.type == 'current' %}
<h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
{% if post.content contains site.excerpt_separator %}
{{ post.excerpt }}
<a href="{{ post.url }}">Read more...</a>
{% else %}
{{ post.content }}
{% endif %}
{% endif %}
{% endfor %}

---

## Past projects

{% for post in site.posts %}
{% if post.type == 'past' %}
<h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
{% if post.content contains site.excerpt_separator %}
{{ post.excerpt }}
<a href="{{ post.url }}">Read more...</a>
{% else %}
{{ post.content }}
{% endif %}
{% endif %}
{% endfor %}
