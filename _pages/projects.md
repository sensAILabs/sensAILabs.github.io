---
title: "SensAILabs - Projects"
layout: gridlay
excerpt: "SensAILabs @ UofT"
sitemap: false
permalink: /projects/
---

# Projects


<div class="row row-cols-1 row-cols-md-3 g-4 mb-3" markdown="0">
    {% for project in site.projects %}
        <div class="col">
            <div class="card">
                <div class="card-body" style="min-height: 250px">
                    <h5 class="card-title">{{ project.title }}</h5>
                    <p class="card-text"> {{ project.excerpt }} </p>
                    <a style="position: relative;bottom: 0" href="{{ project.url }}"> Learn More... </a>
                </div>
                <div class="card-footer d-flex flex-row flex-wrap justify-content-center">
                    {% for member in project.members %}
                        {% if site.data.team_members[member] %}


                        <div class="mx-2">
                            <a href="{{ site.data.team_members[member].page }}" style="text-decoration: none">
                                <img class="rounded-circle profile" alt="{{ site.data.team_members[member].name }}"
                                     title="{{ site.data.team_members[member].name }}"
                                     src="{{ site.data.team_members[member].photo }}"
                                     style="width: 40px; height: 40px; object-fit: cover;">
                            </a>
                        </div>
                          {% endif %}
                    {% endfor %}
                </div>

            </div>
        </div>
    {% endfor %}

</div>
