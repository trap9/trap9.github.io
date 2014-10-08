---
layout: page
title: Archive
description: "An archive of all posts."
---
## Blog posts archive

{% for post in site.posts %}
<!-- Look the author details up from the site config. -->
{% assign author = site.data.authors[post.author] %}
  * {{ post.date | date_to_string }} {{author.name}} &raquo; [ {{ post.title }} ]({{ post.url }})
{% endfor %}
