---
layout: default
title: Projects
section: projects
---

<h1>Projects</h1>

<p>
    A collection of games, software, experiments, and other things I've
    worked on.
</p>

{% for project in site.projects %}

<table class="project-card">
<tr>
<td class="project-card-heading">
<strong>{{ project.title }}</strong>
{% if project.date %}
<span> - {{ project.date | date: "%m/%Y" }}</span>
{% endif %}
</td>

<td class="project-card-info">
<a href="{{ project.url | relative_url }}">More info</a>
</td>
</tr>

<tr>
<td colspan="2" class="project-card-description">
{{ project.excerpt | strip_html | strip_newlines | truncatewords: 60 }}
</td>
</tr>
</table>

{% endfor %}