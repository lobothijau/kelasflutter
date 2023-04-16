---
layout: page
title: Articles by Bagus Aji Santoso
---

Halo semua, nama saya **Bagus**! Saya adalah seorang *mobile application developer* yang juga hobi oprak-oprek banyak teknologi lainnya. Blog yang kalian baca saat ini adalah salah wadah tulisan-tulisan saya yang fokus pada bidang *mobile application development* khususnya dengan framework Flutter. 
{: .has-text-centered}

Cari tahu lebih lanjut tentang saya di [bagusaji.dev](https://www.bagusaji.dev) atau hubungi saya lewat [Twitter](https://www.twitter.com/gusajisan) atau [LinkedIn](https://linkedin.com/in/baguzzzaji). 
{: .has-text-centered}

----
  
# Latest Articles
{: .mb-6 .title .has-text-centered}

{% posts = collections.posts.resources[0...4] %}
{%= liquid_render "bulmatown/collection", collection: posts, metadata: site.metadata %}

{% if collections.posts.resources.size > 4 %}
  <a href="/articles" class="button is-primary is-outlined is-small"><span>Previous Articles</span> <span class="icon"><i class="fa fa-arrow-right"></i></span></a>
  {: .mt-6 .has-text-centered}
{% end %}
