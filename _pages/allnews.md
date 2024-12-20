---
title: "News"
layout: textlay
excerpt: "TSI Lab at Ningbo University."
sitemap: false
permalink: /allnews.html
---

# News

{% for article in site.data.news %}
  <div class="article-content">
    <span class="article-date">{{ article.date }}</span><br>
    <span class="article-headline">{{ article.headline | markdownify }}</span>
  </div>
{% endfor %}
