---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}


------

<h1>Conference Papers</h1>
{% for post in site.publications reversed %}
  {% if post.pubtype == 'conference' %}
      {% include archive-single.html %}
  {% endif %}
{% endfor %}

------

<h1>Journal Papers</h1>
{% for post in site.publications reversed %}
  {% if post.pubtype == 'journal' %}
      {% include archive-single.html %}
  {% endif %}
{% endfor %}

------
<h1>Preprints</h1>
{% for post in site.publications reversed %}
  {% if post.pubtype == 'preprint' %}
      {% include archive-single.html %}
  {% endif %}
{% endfor %}

------

<sup>*</sup> Equal contribution