---
layout: content_page
permalink: /debug
topnav: home
sponsors: "off"
image:
  feature: basic-logo.png
---


{% assign testurl = "/images/"|append: page.image.feature | relative_url %}

| variable  |  value |
|:----------:|:-------|
|site.url | {{ site.url }}|
|site.baseurl | {{ site.baseurl }} |
|site.relativeurl | {{ site.relativeurl }} |
|site.grid_styles | {{ site.grid_styles|join: "," }} |
|site.tags | {{ site.tags }} |

* "/images/"|append: page.image.feature \| relative_url is '{{ testurl }}'
