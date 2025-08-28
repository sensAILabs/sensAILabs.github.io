---
title: "SensAILabs - News"
layout: textlay
excerpt: "SensAILabs @ UofT"
sitemap: false
permalink: /news/
---

# News

{% for article in site.data.news %}
<p markdown="0" >{{ article.date }} <br> {{ article.headline | markdownify}}
</p>
{% endfor %}
