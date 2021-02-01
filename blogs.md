---
layout: content_page
topnav: community.blogs
permalink: /blogs
banner: Bloggin' away
image:
  feature: "CornwallisLetterHead.png"
---

<div class="row">
{% for post in site.categories.articles %}
  <!-- post.path is {{post.path}} -->
  {% for p in post %}
  <!-- p is {{p}} -->
  {%endfor %}
  {% unless post.path contains "example" %}
    <div class="grid_9">
    {% include post-grid.html %}
    </div>
  {% endunless %}
{% endfor %}
</div>
