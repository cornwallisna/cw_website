---
layout: content_page
permalink: /debug
topnav: home
sponsors: "off"
image:
  feature: basic-logo.png
---


{% assign testurl = "/images/"|append: page.image.feature | relative_url %}
{% assign test2url = page.image.feature | relative_url %}

| variable  |  value |
|:----------:|:-------|
|site.url | {{ site.url }}|
|site.baseurl | {{ site.baseurl }} |
| link with baseurl | <a href="{{site.baseurl}}/images/{{page.image.feature}}"> {{page.image.feature}}</a>|
|leading slash | <a href="/images/{{page.image.feature}}"> {{page.image.feature}}</a>|
| no leading slash | <a href="images/{{page.image.feature}}"> {{page.image.feature}}</a>|
|site.grid_styles | {{ site.grid_styles|join: "," }} |
|site.tags | {{ site.tags }} |

* "/images/"|append: page.image.feature \| relative_url is '{{ testurl }}'
* page.image.feature \| relative_url is '{{ test2url }}'
