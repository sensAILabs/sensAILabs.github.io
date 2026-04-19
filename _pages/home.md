---
title: "SensAILabs - Home"
layout: homelay
excerpt: "SensAILabs @ UofT"
sitemap: false
permalink: /
---

<!-- HERO SLIDER AT TOP -->
<div id="heroCarousel" class="carousel slide page-hero" data-bs-ride="carousel" markdown="0">
  <div class="carousel-inner">
    <!-- Slide 1 -->
    <div class="carousel-item active">
      <img src="/images/slider/sensailab_fall2025.jpg" class="d-block w-100 page-hero-img" alt="Slide 1">
      <span class="hero-overlay">Kicking off Fall 2025 together with Prof. Kuimi and Prof. Mitani.</span>
    </div>
    <!-- Slide 2 -->
    <div class="carousel-item">
      <img src="/images/slider/sensai_grad2025.jpg" class="d-block w-100 page-hero-img" alt="Slide 2">
      <span class="hero-overlay">Congratulations and Happy Graduation to our Students!</span>
    </div> 
    <!-- Slide 3 -->
    <div class="carousel-item">
      <img src="/images/slider/sensai_youthoutreach2025.jpg" class="d-block w-100 page-hero-img" alt="Slide 3">
      <span class="hero-overlay">Syed @ DLSPH Youth Outreach Program 2025</span>
    </div> 
  </div>

  <!-- Prev/Next controls -->
  <button class="carousel-control-prev" type="button" data-bs-target="#heroCarousel" data-bs-slide="prev">
    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
    <span class="visually-hidden">Previous</span>
  </button>
  <button class="carousel-control-next" type="button" data-bs-target="#heroCarousel" data-bs-slide="next">
    <span class="carousel-control-next-icon" aria-hidden="true"></span>
    <span class="visually-hidden">Next</span>
  </button>
</div>

<hr class="quote-divider" markdown="0">
    
<div class="quote-section text-center" markdown="0">
    <blockquote class="blockquote">
        <font face="Lucida Handwriting, Cursive">
        <p>“When I want to understand what is happening today or try to decide what will happen tomorrow, I look back.”</p>
        <footer>– Omar Khayyam (Mathematician, Philosopher)</footer>
        </font>
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
