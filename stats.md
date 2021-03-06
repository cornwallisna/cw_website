---
layout: content_page
topnav: home
hitID: stats
title: Stats
permalink: /stats
sponsors: "off"
---

# Site Statistics


|Page Title(path) | Hits | uniqID |
|:----------|:-------|:-----|
{%- for p in site.pages -%}
 {%- assign hitID =  p.hitID | default: p.permalink | strip | replace: " ","" | downcase| prepend: "page_"  -%}
 {%- assign hitURL = site.github_url | append: 'hit-counter-' | append: hitID | url_encode %}
| {{ p.name }} ({{p.permalink}}) |  <img src="https://hitcounter.pythonanywhere.com/nocount/tag.svg?url={{ hitURL}}" alt="Users"> | {{ hitURL }} |
{%- endfor %}
