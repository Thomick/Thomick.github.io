---
layout: archive
title: "Sitemap"
permalink: /sitemap/
author_profile: true
---

{% include base_path %}

A list of all the posts and pages found on the site. For you robots out there is an [XML version]({{ base_path }}/sitemap.xml) available for digesting as well.

<h2>Pages</h2>

{% assign pages = site.pages | sort: 'title' %}
{% for post in pages%}
  {% if post.sitemap != false %}
  {% include archive-single.html %}
  {% endif %}
{% endfor %}

{% if site.posts.size > 0  %}
<h2>Posts</h2>
{% assign posts = site.posts | sort: 'title' %}
{% for post in posts %}
  {% include archive-single.html %}
{% endfor %}
{% endif %}

{% capture written_label %}'None'{% endcapture %}

{% for collection in site.collections %}
{% if collection.docs.size > 0 %}
{% unless collection.output == false or collection.label == "posts" %}
  {% capture label %}{{ collection.label }}{% endcapture %}
  {% if label != written_label %}
  <h2>{{ label | capitalize }}</h2>
  {% capture written_label %}{{ label }}{% endcapture %}
  {% endif %}
{% endunless %}
{% for post in collection.docs %}
  {% unless collection.output == false or collection.label == "posts" %}
  {% include archive-single.html %}
  {% endunless %}
{% endfor %}
{% endif %}
{% endfor %}
