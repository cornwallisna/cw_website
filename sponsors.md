---
layout: content_page
topnav: sponsors
banner: A special thanks to our sponsors
permalink: /sponsors
sponsors: "off"
---



{% for slide in site.data.sponsors.slides %}

<h2> <a href="{{slide.link}}">{{slide.name}}</a> </h2>

<div class="row">
<div class="grid_7">
<a href="{{slide.link}}"><img src="{{slide.img}}" width="70%" style="float: left;"></a>
</div>
<p/>
<div class="grid_5"> {{slide.caption}} </div>
</div>
<p>

{% endfor %}
