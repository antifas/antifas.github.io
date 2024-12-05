---
title: Contato
layout: page
feature_image: "imgs/banda.jpg"
---

<ul>
{% for link in site.social_links %}
{% if link[1] != blank %}
{% assign id = link[0] | downcase %}
<a href="{{ link[1] }}">
<li>
{% include icon.html id=id title=id %}
{{ id }} - {{ link[1] }}
</li>
</a>
{% endif %}
{% endfor %}
</ul>


