---
title: "Allan Lab - Projects"
layout: gridlay
excerpt: "Allan Lab -- Projects."
sitemap: false
permalink: /projects/
---

# Projects

<div class="row row-cols-1 row-cols-md-3 g-4 mb-3" markdown="0">
              {% for project  in site.data.projects %}
    <div class="col" >
        <div class="card">
            <div class="card-body" style="min-height: 180px"  >
                <h5 class="card-title">{{ project.title }}</h5>
                <p class="card-text"> {{ project.description    |  truncate: 200 }} </p>
            </div>
           <div class="card-footer d-flex flex-row flex-wrap justify-content-center">
                    {% for member in project.members %}
                        <div class="mx-2">
                            <a href="{{ site.data.team_members[member].page }}" style="text-decoration: none">
                                <img class="rounded-circle profile" alt="{{ site.data.team_members[member].name }}" title="{{ site.data.team_members[member].name }}"
                                    src="{{ site.data.team_members[member].photo }}" style="width: 40px; height: 40px; object-fit: cover;">
                            </a>
                        </div>
                    {% endfor %}
                </div>

        </div>
    </div>
{% endfor %}

</div>
