---
layout: page
title: Contributors
permalink: /contributors/
---

This page holds a list of all the lovely contributors to the site :)

<section>
{% for contributor in site.github.contributors %}
    <div>
        <a target="_blank" href="{{ contributor.html_url }}">
            <img src="{{ contributor.avatar_url }}" width="48px" height="48px" /> {{ contributor.login }} 
        </a>
    </div>
{% endfor %}
</section>
