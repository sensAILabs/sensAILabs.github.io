---
title: "News"
layout: textlay
excerpt: "Allan Lab at Leiden University."
sitemap: false
permalink: /news/
---

# News

{% for article in site.data.news %}
<p markdown="0" >{{ article.date }} <br> {{ article.headline | markdownify}}
</p>
{% endfor %}