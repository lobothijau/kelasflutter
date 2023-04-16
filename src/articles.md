---
layout: page
title: Tutorial Pemrograman Flutter
subtitle: Buat aplikasi <em>mobile cross platform</em> untuk Android & iOS.
exclude_from_search: true
paginate:
  collection: posts
---

{% posts = paginator.resources %}
{%= liquid_render "bulmatown/collection", collection: posts, metadata: site.metadata %}

{%= liquid_render "bulmatown/pagination", paginator: paginator %}