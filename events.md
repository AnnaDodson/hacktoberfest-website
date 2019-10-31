---
layout: page
title: Events
permalink: /events/
---

This page holds a list of all the lovely Hacktoberfest events in Nottingham 🙃

<section class="events_list">

  <div class="event_outer">
    {% assign sorted_events = site.data.events | sort: 'date' | reverse %}
    {% for event in sorted_events %}
    {% capture nowunix %}{{ 'now' | date: '%s' }}{% endcapture %}
    {% capture eventtime %}{{ event.date | date: '%s' }}{% endcapture %}
    <a target="_blank" href="{{ event.url }}" title="{{ event.title }}" class="event {% if eventtime < nowunix %}event--done{% endif %}">
      <div class="event_date">
        <span class="event_date--value">
        {% assign day = event.date | date: "%-d"  %}
        {% case day %}
          {% when '1' or '21' or '31' %}{{ day }}st
          {% when '2' or '22' %}{{ day }}nd
          {% when '3' or '23' %}{{ day }}rd
          {% else %}{{ day }}th
        {% endcase %}
        </span>
      </div> 
      <h2 class="event_title">{{ event.title }}</h2>
      <p class="event_description">{{ event.description }}</p>
    </a>
    {% endfor %}
  </div>

</section>

<script>
    const events = document.querySelectorAll('.event');
    const now = new Date();

    // Loop through events
    events.forEach(event => {
        const endDate = new Date(event.dataset.endDate);

        // If end date is in the past, add class to style it
        if (now > endDate) {
            event.classList.add('event--done');
        }
    })
</script>
