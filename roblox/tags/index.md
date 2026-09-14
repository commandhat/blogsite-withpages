---
layout: default
title: Roblox Tags
section: roblox
---

<h1>Roblox Tags</h1>

<p>
Browse Roblox reviews by tag.
</p>

{% assign all_tags = "" | split: "" %}

{% for review in site.roblox %}
{% for tag in review.tags %}
{% assign all_tags = all_tags | push: tag %}
{% endfor %}
{% endfor %}

{% assign all_tags = all_tags | uniq | sort %}

<ul>
{% for tag in all_tags %}
<li>
<a href="{{ '/roblox/tags/' | relative_url }}{{ tag | slugify }}/">
{{ tag }}
</a>
</li>
{% endfor %}
</ul>