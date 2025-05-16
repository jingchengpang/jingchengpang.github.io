---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

<span id="top" style="position: absolute; top: 0; opacity: 0;"></span>

<style>
#top {
  top: -100px;
}
</style>

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

------

<h1>Preprints</h1>
{% for post in site.publications reversed %}
  {% if post.pubtype == 'preprint' %}
      {% include archive-single.html %}
  {% endif %}
{% endfor %}


------

<h1>Conference/Journal Papers</h1>
{% for post in site.publications reversed %}
  {% if post.pubtype == 'conference' or post.pubtype == 'journal' %}
      {% include archive-single.html %}
  {% endif %}
{% endfor %}

------

<h1>Manuscripts</h1>
{% for post in site.publications reversed %}
  {% if post.pubtype == 'manuscript' %}
      {% include archive-single.html %}
  {% endif %}
{% endfor %}

------


[[Back to top](#top)]