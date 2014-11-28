---
layout: page
title: Bio(s)
---

<p class="message">
  Please, leave comments - give me an opportunity to say a thank you :-)
</p>

<div>
 <a name="jiri_zoth"></a><h3 class="bio-icon-left">Jiri Zoth</h3>
 <a class="bio-icon-right" href="http://linkedin.com{{ site.data.authors.jiri_zoth.linkedin }}">{% include svg-icons/linkedin.html %} </a>
</div>
*an enthusiastic ethical liberal subconsciously  roaming over fields of responsibility inflected by society's compulsion.*

*Don't get it? Neither do I.*

![photo](/assets/img/jiri_zoth.png)

A more elaborative (aka boring) description of myself:

* An entrepreneur - software, computer vision, electronics, augmented reality, immersion computing,
* husband,
* father,
* and hedonist.

... and some ex, which some becoming manifested again :-)

* A runner, windsurfer, snowboarder, mountain hiker, floor-,volley-,basketball player, student of karate,
* idealist,
* analyst, manager, programmer,
* chess&go player, mathematician and physicist.

Likes

* programming - issue cracking
* electronics
* math and physics
* wine, whisky and rum
* books, movies
* similar people
* family
* running

Hates

* repetition of any kind
* imperfection
* waking up
* people of a style, which is so cliché I am not gonna name it.
* exercises of any kind

### My articles

{% for post in site.posts %}
{% if post.author == 'jiri_zoth' %}
&raquo; [ {{ post.title }} ]({{ post.url }}) {{ post.date | date_to_string }}
{% endif %}
{% endfor %}

---
