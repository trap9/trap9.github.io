---
layout: page
title: Bio(s)
---

<p class="message">
  Please, leave comments - give me an opportunity to say a thank you :-)
</p>


### <a name="jiri_zoth"></a>Jiri Zoth

*an enthusiastic ethic liberal subconsciously  roaming over fields of responsibility inflected by society compulsion.*

*Don't get it? Neither do I.*

![photo](/assets/photo2.png)

In more elaborative (aka boring) description of myself:

* An entrepreneur - software, computer vision, electronics, augmented reality, immersion computing,
* husband,
* father,
* and hedonist.

... and some ex, which some becoming manifested again :-)

* A runner, windsurfer, snowboarder, mountain hiker, floor&volley&basketball player, karate,
* idealist,
* analyst, manager, programmer,
* chess&go player, mathematician and physicist.

Likes

* programming - issue cracking
* electronics
* math and physics
* vine, whisky and rum
* books, movies
* people of such kind
* family
* running

Hates

* repetition of any kind
* imperfection
* wake up
* people of a kind, which is so cliché I am not gonna name it.
* exercises of any kind

### My articles

{% for post in site.posts %}
{% if post.author == 'jiri_zoth' %}
&raquo; [ {{ post.title }} ]({{ post.url }}) {{ post.date | date_to_string }}
{% endif %}
{% endfor %}

---
