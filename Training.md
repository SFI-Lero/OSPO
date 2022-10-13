---
layout: default
title: "Events"
description: "The LERO OSPO community"
logo:
header-img:
ordernumber: 4
---

{% assign sorted_events = site.events | sort: "start_date" | reverse %}
{% assign today = "now" | date: "%d-%m-%Y" %}

<section class="py-5">
  <div class="custom-container">
    <h2 class="mb-3 text-center">Upcoming Events</h2>
  </div>
  <div class="custom-container">
    <div class="row">
      {% for event in sorted_events%}
        {% if event.start_date > today %}
          <div class="col-sm-12 col-md-6 col-lg-4 mb-4">
            {% if event.default_image %}
              <div class="card text-white card-has-bg click-col" style="background-image:url('/OSPO/img/events/{{event.default_image}}');">
            {% else %}
              <div class="card text-white card-has-bg click-col" style="background-image:url('/OSPO/img/events/{{event.image}}');">
            {% endif %}
              <a class="text-white" href="/OSPO{{event.url}}">
              <div class="card-img-overlay d-flex flex-column">
                <div class="card-body">
                  <h4 class="card-meta mb-2">{{event.name}}</h4>
                  <small class="text-underline">
                    <u>
                      <i class="far fa-clock"></i> 
                      {{event.start_date  | date: "%-d %B %Y" }} {% if event.end_date %} - {{event.end_date  | date: "%-d %B %Y" }} {% endif %}
                    </u>
                  </small>
                  <small class="card-title mt-0 "><p>{{event.short_description}}</p></small>
                </div>
              </div>
              </a>
            </div>
          </div>
        {% endif %}
      {% endfor %}
    </div>
  </div>
</section>
<section class="py-5">
  <div class="custom-container">
    <h2 class="mb-3 text-center">Past Events</h2>
  </div>
  <div class="custom-container">
    <div class="row">
      {% for event in sorted_events%}
        {% if event.start_date < today %}
        <div class="col-sm-12 col-md-6 col-lg-4 mb-4">
          {% if event.default_image %}
            <div class="card text-white card-has-bg click-col" style="background-image:url('/OSPO/img/events/{{event.default_image}}');">
          {% else %}
            <div class="card text-white card-has-bg click-col" style="background-image:url('/OSPO/img/events/{{event.image}}');">
          {% endif %}
            <a class="text-white" href="/OSPO{{event.url}}">
            <div class="card-img-overlay d-flex flex-column">
              <div class="card-body">
                <h4 class="card-meta mb-2">{{event.name}}</h4>
                <small class="text-underline">
                  <u>
                    <i class="far fa-clock"></i> 
                    {{event.start_date  | date: "%-d %B %Y" }} {% if event.end_date %} - {{event.end_date  | date: "%-d %B %Y" }} {% endif %}
                  </u>
                </small>
                <small class="card-title mt-0 "><p>{{event.short_description}}</p></small>
              </div>
            </div>
            </a>
          </div>
        </div>
      {% endif %}
      {% endfor %}
    </div>
  </div>
</section>
