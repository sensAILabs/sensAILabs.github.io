---
title: "SensAILabs - Home"
layout: homelay
excerpt: "SensAILabs @ UofT"
sitemap: false
permalink: /
---

<hr class="quote-divider" markdown="0">

<div class="quote-section text-center" markdown="0">
    <blockquote class="blockquote">
        <p>“When I want to understand what is happening today or try to decide what will happen tomorrow, I look back.”</p>
        <footer>– Omar Khayyam (Mathematician, Philosopher)</footer>
    </blockquote>
</div>

<hr class="quote-divider" markdown="0">

<div class="main-back" markdown="0">
    <div class="row">
        <div class="col-lg-1 col-md-1 col-sm-0"></div>
        <div class="col-lg-10 col-md-10 col-sm-12">
            <p>
                Our research commits to innovative, responsibly AI-driven health systems powered by ubiquitous computing. We look back at the data collected from our prototype devices to make sense of past events and anticipate future developments for the benefit of public health. If that sounds daunting, don’t worry. We provide the caffeine, the algorithms, and just enough chaos to keep things interesting while we tackle these challenges together. Join us!
            </p>
        </div>
    </div>
</div>

<div class="row row-cols-1 row-cols-md-3 g-4 mb-3" markdown="0">
    {% for project in site.projects %}
        <div class="col">
            <div class="card">
                <div class="card-body" style="min-height: 250px">
                    <h5 class="card-title">{{ project.title }}</h5>
                    <p class="card-text"> {{ project.summary }} </p>
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

<hr class="quote-divider" markdown="0"/>

## News Update

<ul style="padding: 0 10vh" class="wp-block-list">
    {% for news in site.data.news %}
        {% if forloop.index0 < 5 %}
            <li>{{ news.headline }}<br><em>– {{ news.date }} </em></li>
        {% endif %}
    {% endfor %}
    <li><a href="/news"> More ... </a></li>
</ul>

## Funding Support

<div class="container logos" style="margin-top: 1vw" markdown="0">
    <div class="row text-center justify-content-center">
        <!-- Logo 1 -->
        {% for logo in site.data.logos %}
            <div class="col-xs-12 col-sm-4 col-md-3 col-lg-3 " style="padding: 10px;">
            <a target="_blank" href="{{ logo.url }}">    <img src="{{ logo.image }}" class="img-fluid"
                     alt="{{ logo.name }}">
                </a>
            </div>
        {% endfor %}


    </div>
</div>

<hr class="quote-divider">
