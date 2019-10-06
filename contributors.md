---
layout: page
title: Contributors
permalink: /contributors/
---

This page holds a list of all the lovely contributors to the site 🙃

<section class="contributors_grid">
{% for contributor in site.github.contributors %}
    <div class="contributor">
     <img src="{{ contributor.avatar_url }}" width="48px" height="48px" alt="{{contributor.login}} GitHub profile"/>
        <a target="_blank" href="{{ contributor.html_url }}" title="GitHub profile for {{ contributor.login }} ">
            {{ contributor.login }} 
        </a>
    </div>
{% endfor %}
</section>
