---
layout: default
title: Home
---

# Commandhat

This is my personal website.

I write about games, programming, projects, and other things I'm working on.

## Recent writing

{% assign recent_posts = site.blog | sort: "date" | reverse %}

{% for post in recent_posts limit: 5 %}
### [{{ post.title }}]({{ post.url | relative_url }})

{{ post.excerpt }}

{% endfor %}