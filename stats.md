---
title: Stats
---

# Site Statistics


|Page Title(path) | Hits | uniqID |
|:----------|:-------|:-----|
{%- for p in site.pages -%}
 {%- assign hitID =  p.hitID | default: p.permalink | strip | replace: " ","" | downcase| prepend: "page_"  -%}
 {%- assign hitURL = site.github_url | append: 'hit-counter-' | append: hitID | url_encode %}
| {{ p.name }} ({{p.permalink}}) |  <img src="https://hitcounter.pythonanywhere.com/nocount/tag.svg?url={{ hitURL}}" alt="Users"> | {{ hitURL }} |
{%- endfor %}
