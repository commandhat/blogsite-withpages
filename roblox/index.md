---
layout: default
title: Roblox - Diamonds in the Dirt
section: roblox
---

<h1>Roblox: Diamonds in the Dirt</h1>

<p>
    I'm over 30 years old, but a little over half my life has been spent on
    and around the online MMOG Roblox. Every passing day, it gets harder to
    find an actually fun game buried amongst the clicker games with millions
    of buttons that ask for you to open your wallet.
</p>

<p>
    As such, I wanted a section on my website to highlight the rare games I
    find that have gameplay beyond the usual "Buy Robux" interface. The
    diamonds (fun games), if you prefer, that are hidden in the dirt (the
    games browser).
</p>

<h2>Latest Posts</h2>

{% for post in site.roblox %}
{% assign review_score = post.gamescore | plus: post.viewscore | plus: post.techscore | plus: post.timescore | plus: post.devxscore %}
{% assign best_score = post.gamescore %}
{% assign best_category = "Gameplay" %}

{% if post.viewscore > best_score %}
{% assign best_score = post.viewscore %}
{% assign best_category = "Art" %}
{% endif %}

{% if post.techscore > best_score %}
{% assign best_score = post.techscore %}
{% assign best_category = "Technical" %}
{% endif %}

{% if post.timescore > best_score %}
{% assign best_score = post.timescore %}
{% assign best_category = "Time" %}
{% endif %}

{% if post.devxscore > best_score %}
{% assign best_score = post.devxscore %}
{% assign best_category = "DevEx" %}
{% endif %}

<table class="roblox-review-card">
<tr class="roblox-card-main">
<td class="roblox-card-thumbnail">
{% if post.game_thumbnail %}
<img
src="{{ post.game_thumbnail | relative_url }}"
alt="{{ post.game_title }} thumbnail"
>
{% endif %}
</td>

<td colspan="2" class="roblox-card-game">
<div class="roblox-card-heading">
<h3>{{ post.game_title }}</h3>

<a
href="{{ post.url | relative_url }}"
class="roblox-card-link"
>
Read Review
</a>
</div>

{% if post.game_description %}
<p>{{ post.game_description }}</p>
{% endif %}
</td>
</tr>

<tr class="roblox-card-review">
<td colspan="3">
{% if post.review_description %}
<p>{{ post.review_description }}</p>
{% endif %}
</td>
</tr>

<tr class="roblox-card-meta">
<td>
<strong>{{ review_score }}% (Best: {{ best_category }} {{ best_score }}/20)</strong>
</td>

<td>
{{ post.date | date: "%B %-d, %Y" }}
</td>

<td>
{% if post.version %}
{{ post.version }}
{% endif %}
</td>
</tr>
</table>

{% endfor %}