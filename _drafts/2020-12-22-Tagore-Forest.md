---
layout: post
title: Tagore Forest
is_series: true
series_title: "Disappearing Habitats"
---

## Tagore Forest

Sandwiched between the Central Catchment Nature Reserve and the forests of Sungei Seletar, Tagore is a massive forest patch of immense biodiversity value.

<!-- Series links -->
{% if page.is_series == true %}
<h3 class="text-success p-3 pb-0">{{ page.series_title | upcase }} series</h3>
{% assign posts = site.posts | where: "is_series", true | where: "series_title", page.series_title | sort: 'date' %}
 
{% for post in posts %}
        {% if post.title == page.title %}
 <p class="nav-link bullet-pointer mb-0">{{ post.title }}</p>
        {% else %}
 <a class="nav-link bullet-hash" href="{{ post.url }}">{{ post.title }}</a>
        {% endif %}
{% endfor %}

{% endif %}