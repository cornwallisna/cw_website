---
layout: content_page
topnav: news
permalink: /news
banner: All the CNA news that is fit to print
image:
  feature: "monument.png"
---

## If you have a life event you would like to share ...
Please send us the details and pictures if any to our [Editors](mailto:cornwallisna+lifeevents@gmail.com) for inclusion here.

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
