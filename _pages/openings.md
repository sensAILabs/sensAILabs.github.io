---
title: "SenseAI Lab - Vacancies"
layout: textlay
excerpt: "Openings"
sitemap: false
permalink: /vacancies
---
{% comment %}<div class="row" style="padding: 0 100px">{% endcomment %}
{% comment %}<div class="col-lg-6" > <figure>{% endcomment %}
{% comment %}<img src="{{ site.url }}{{ site.baseurl }}/images/picpic/Gallery/utarmsIB.jpg" width="95%">{% endcomment %}
{% comment %}</figure> </div>{% endcomment %}
{% comment %}<div class="col-lg-6" > <figure>{% endcomment %}
{% comment %}<h3>1924 June 5</h3>{% endcomment %}
{% comment %}The dedication of Soldier's Tower in University of Toronto is an impressive event, with detachments of the militia units of Toronto present. Their slow march from Knox College to the front of the tower is proceeded by bands of the Governor-General's Body Guard and the Forty-Eighth Highlanders, and numerous dignitaries.{% endcomment %}
{% comment %}</figure> </div>{% endcomment %}
{% comment %}</div>{% endcomment %}

# Open positions

**We have open positions for the following projects: **

{% for project in site.projects %}
{% if project.opening %}
## [{{ project.title }}]({{ project.url }}) <br>
{% endif %}
{% endfor %}

