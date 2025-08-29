---
title: "SensAILabs - Publications"
layout: gridlay
excerpt: "SensAILabs @ UofT"
sitemap: false
permalink: /publications/
---

# Publications

{% for project in site.data.publist %}<p class="d-inline-flex gap-1">
        <a class="icon-link icon-link-hover" data-bs-toggle="collapse" href="#collapse{{ forloop.index0 }}" role="button"
           aria-expanded="false" aria-controls="collapse{{ forloop.index0 }}">
            {{ project[0] }} <i class="fa-solid fa-arrow-right"></i>
        </a>
    </p><div class="collapse" id="collapse{{ forloop.index0 }}">
 <div class="card card-body" markdown="0" >{% for pub in  project[1]  %}<div class="row">
                <div class="col-sm-10">
                    <div style="font-weight: bolder;" >    {{  pub.title }}
                    </div>

                         <em> {{  pub.periodical }} </em><br>
                         <em> {{  pub.authors }} </em>


                    <div class="links-pub">

                        {% for lnk in  pub.links  %}
                                <a href="{{ lnk.first[1] }}"
                           class="btn btn-sm z-depth-0" role="button">{{ lnk.first[0] }}</a>
                        {% endfor %}

                    </div>

                </div>
            </div>
    {% endfor %}
        </div>
</div>
{% endfor %}

