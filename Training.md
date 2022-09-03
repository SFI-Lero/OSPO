---
layout: default
title: "Events"
description: "The LERO OSPO community"
logo:
header-img:
ordernumber: 4
---

{% assign sorted_events = site.events | sort: "date" %}

<section class="py-5">
  <div class="custom-container">
    <h2 class="mb-3 text-center">Events</h2>
    <!-- <p class="text-justify">
      An event is something that happens, especially when it is unusual or important. You can use events to describe
      all the things that are happening in a particular situation.
    </p> -->
  </div>
  <div class="custom-container">
    <div class="row">
      {% for event in sorted_events%}
        <div class="col-sm-12 col-md-6 col-lg-4 mb-4">
          <div class="card text-white card-has-bg click-col"
            style="background-image:url('https://source.unsplash.com/600x900/?tech,street');">
            <img class="card-img d-none" src="https://source.unsplash.com/600x900/?tech,street"alt="random">
            <div class="card-img-overlay d-flex flex-column">
              <div class="card-body">
                <h4 class="card-meta mb-2">{{event.name}}</h4>
                <small class="card-title mt-0 "><a class="text-white" href="/OSPO/{{event.url}}">{{event.short_description}}</a></small>
                <small class="text-underline"><i class="far fa-clock"></i> {{event.date}} </small>
              </div>
              <!-- <div class="card-footer">
                <div class="media">
                  <div class="media-body">
                    <h6 class="my-0 text-white d-block">Organizer</h6>
                    <small>Organiz description</small>
                  </div>
                </div>
              </div> -->
            </div>
          </div>
        </div>
      {% endfor %}
    </div>
  </div>

</section>
