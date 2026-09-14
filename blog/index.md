---
layout: default
title: Blog
section: blog
---

<h1>My Thoughts & Writings</h1>

<p>
    A collection of ongoing thoughts, memes, and articles written on various
    topics.
</p>

<h2>Latest Posts</h2>

{% for post in site.blog %}

{% assign word_count = post.content | number_of_words %}

<article class="blogroll-entry">

<h3>
<a href="{{ post.url | relative_url }}">{{ post.title }}</a>
</h3>

<p class="blogroll-meta">
{{ post.date | date: "%B %-d, %Y" }} · {{ word_count }} words
</p>

<p>
{{ post.excerpt | strip_html | strip_newlines | truncatewords: 40 }}
</p>

<p>
<a href="{{ post.url | relative_url }}">Read more</a>
</p>

</article>

{% endfor %}