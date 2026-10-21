---
layout: page
title: Latest News
---

{% comment %}
To add an announcement, create a file in _posts/ named YYYY-MM-DD-short-title.md
and copy the front matter of an existing post. The three newest also appear on the home page.
{% endcomment %}
{:.intro-text}
Announcements and updates about the workshop.

<div class="news-list">
{%- for post in site.posts %}
{% include news_card.html post=post %}
{%- endfor %}
</div>
