---
layout: page
title: blog
description: Let's talk.
permalink: /blog/
---


{% for blog in site.blog %}
  <h2>{{ blog.title }}</h2>
  <p>Performed by {{ blog.artist }} {% if blog.director %}, directed by {{ blog.director }}{% endif %}</p>
  {% for work in blog.works %}

<h3>{{ work.title }}</h3>
<p>Composed by {{ work.composer }}</p>
<ul>
{% for track in work.tracks %}
<li>{{ track.title }} ({{ track.duration }})</li>
{% endfor %}
</ul>
  {% endfor %}
{% endfor %}