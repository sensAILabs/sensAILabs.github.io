---
title: "SensAILabs - Team"
layout: gridlay
excerpt: "SensAILabs @ UofT"
sitemap: false
permalink: /team/
---

# Who Are We?
{% assign number_printed = 0 %}
{% for member in site.data.team_members %}

    {% if member[1].not_primary or  member[1].is_alumni  %}
       {% continue %}
       {% endif %}
    {% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div  class="teampic col-sm-6 clearfix">
  <img src="{{ member[1].photo }}" class="img-responsive" width="25%" style="float: left;margin-right: 10px" />
   <h4><a style="color: #333333; text-underline: red" href="{{ member[1].page }}"> {{ member[1].name }}</a></h4><i>{{ member[1].info }}</i>

</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}


## Formers
<div class="row">

<div class="col-sm-4 clearfix">

{% for member in site.data.team_members %}
    {% if member[1].is_alumni  %}
{{ member[1].name }} <br>
    <em>- {{ member[1].after_position }}</em>
    {% endif %}
{% endfor %}
</div>


</div>


