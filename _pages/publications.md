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

<h2>Preprints</h2>
{% for post in site.publications %}
  {% if post.pubtype == 'preprint' %}
      {% include archive-single.html %}
  {% endif %}
{% endfor %}


<h2>Conference Papers</h2>
{% for post in site.publications %}
  {% if post.pubtype == 'conference' %}
      {% include archive-single.html %}
  {% else %}
        Not equal to conference
  {% endif %}
{% endfor %}


<h2>Journal Papers</h2>
{% for post in site.publications %}
  {% if post.pubtype == 'journal' %}
      {% include archive-single.html %}
  {% endif %}
{% endfor %}


<sup>*</sup> Equal authorship