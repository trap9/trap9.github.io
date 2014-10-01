---
layout: page
title: Archive
description: "An archive of all posts."
---
## Blog posts archive

{% for post in site.posts %}
  * {{ post.date | date_to_string }} {{post.author}} &raquo; [ {{ post.title }} ]({{ post.url }})
{% endfor %}
