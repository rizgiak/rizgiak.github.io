---
layout: archive
title: "Sitemap"
permalink: /sitemap/
author_profile: true
sitemap: false
---

{% include base_path %}

A list of all the posts and pages found on the site. For you robots out there, there is an [XML version]({{ base_path }}/sitemap.xml) available for digesting as well.

<h2>Pages</h2>
{% for post in site.pages %}
  {% if post.sitemap != false and post.title %}
  {% include archive-single.html %}
  {% endif %}
{% endfor %}

<h2>Posts</h2>
{% for post in site.posts %}
  {% unless post.sitemap == false %}
  {% include archive-single.html %}
  {% endunless %}
{% endfor %}

{% capture written_label %}'None'{% endcapture %}

{% for collection in site.collections %}
{% assign has_public_docs = false %}
{% for post in collection.docs %}
  {% unless post.sitemap == false %}
    {% assign has_public_docs = true %}
  {% endunless %}
{% endfor %}
{% unless collection.output == false or collection.label == "posts" or has_public_docs == false %}
  {% capture label %}{{ collection.label | capitalize }}{% endcapture %}
  {% if label != written_label %}
  <h2>{{ label }}</h2>
  {% capture written_label %}{{ label }}{% endcapture %}
  {% endif %}
{% endunless %}
{% for post in collection.docs %}
  {% unless collection.output == false or collection.label == "posts" or post.sitemap == false %}
  {% include archive-single.html %}
  {% endunless %}
{% endfor %}
{% endfor %}
