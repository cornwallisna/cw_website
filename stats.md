---
layout: content_page
topnav: home
hitID: stats
title: Stats
permalink: /stats
sponsors: "off"
---

# Site Statistics


|Page Title(path) | Hits |
|:----------|:-------|
{%- for p in site.pages -%}
 {%- if p.name contains ".md" -%}
   {%- assign hitID =  p.hitID | default: p.permalink | default: p.name | replace: "/","_" | strip | replace: " ","" | downcase| prepend: "page_"  -%}
   {%- assign hitURL = site.github_url | append: 'hit-counter-' | append: hitID | url_encode %}
| {{ p.name }} ({{p.permalink|default: p.dir}}) |  <img src="https://hitcounter.pythonanywhere.com/nocount/tag.svg?url={{ hitURL}}" alt="Users"> |
 {%-endif -%}
{%- endfor %}

## Raw links

{%- for p in site.pages -%}
 {%- assign hitID =  p.hitID | default: p.permalink | default: p.name |replace: "/","_" | strip | replace: " ","" | downcase| prepend: "page_"  -%}
 {%- assign hitURL = site.github_url | append: 'hit-counter-' | append: hitID | url_encode %}
 <br>
 https://hitcounter.pythonanywhere.com/nocount/tag.svg?url={{ hitURL}}
{%- endfor %}
