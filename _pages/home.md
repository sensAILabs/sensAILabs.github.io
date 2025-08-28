---
title: "SensAILabs - Home"
layout: homelay
excerpt: "SensAILabs @ UofT"
sitemap: false
permalink: /
---
<style markdown="0">
    /* Hide carousel controls but still allow drag */
    .carousel-control {
        display: none;
    }

    {
        overflow: hidden
    ;
    }

    .carousel-inner {
        display: flex;
    }

    .carousel-inner .item {
        display: flex;
        justify-content: space-between;
    }

    /* Ensure the images are responsive and properly sized */
    .carousel-inner img {
        width: 100%;
        height: auto;
        /*border-radius: 0 !important;*/
    }

    .carousel-item img {

        border-radius: 2px !important;
    }
</style>

<div style="padding:0 4vw" markdown="0" id="carousel" class="carousel slide" data-bs-ride="carousel"
     data-bs-interval="4000" data-bs-pause="hover">
    <!-- Menu -->
    <ol class="carousel-indicators">
        {% for slide in site.data.sliders.mainSlider %}
            <li data-bs-target="#carousel" data-bs-slide-to="{{ forloop.index0 }}"
                {% if forloop.first %}class="active"{% endif %}></li>
        {% endfor %}
    </ol>

    <div class="carousel-inner" role="listbox" markdown="0">
        {% for slide in site.data.sliders.mainSlider %}
            <div style="height: 55vh" class="carousel-item {% if forloop.first %}active{% endif %}">
                <img src="{{ slide.image }}" alt="{{ slide.title }}" class="d-block w-100 h-100">
                <div class="carousel-caption d-none d-md-block">
                    <h5>{{ slide.title }}</h5>
                    <p>{{ slide.description }}</p>
                </div>
            </div>
        {% endfor %}
    </div>

    <button class="carousel-control-prev" type="button" data-bs-target="#carousel" data-bs-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Previous</span>
    </button>
    <button class="carousel-control-next" type="button" data-bs-target="#carousel" data-bs-slide="next">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Next</span>
    </button>
</div>

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
                Our research commits to innovative, responsibly AI-driven health systems powered by ubiquitous computing. We look back at the data collected from our prototype devices to make sense of past events and anticipate future developments for the benefit of public health.
            </p>
            <p class="text-left">
                <strong>If you’re curious and driven, we’d love to have you join our team and tackle these challenges.</strong>
                <a href="/projects">(View Projects)</a>!
            </p>
        </div>
    </div>
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
