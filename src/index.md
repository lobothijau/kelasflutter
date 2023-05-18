---
layout: home
exclude_from_search: true
image: "https://mugshotbot.com/m?theme=two_up&mode=light&color=8a1024&pattern=diagonal_lines&image=eed29abf&hide_watermark=true&url=https%3A%2F%2Fwww.fullstackruby.dev"
---

{: .my-6}

{% posts = collections.posts.resources[0...4] %}
{%= liquid_render "bulmatown/collection", collection: posts, metadata: site.metadata %}

{% if collections.posts.resources.size > 4 %}
  <a href="/articles" class="button is-primary is-outlined is-small"><span>Previous Articles</span> <span class="icon"><i class="fa fa-arrow-right"></i></span></a>
  {: .mt-6 .has-text-centered}
{% end %}


<p class="mt-6 is-size-7 has-text-centered"><em>Banner image by <a target=_blank href="https://unsplash.com/photos/DIp71kvwXhU">Aldebaran S on Unsplash</a></em></p>
