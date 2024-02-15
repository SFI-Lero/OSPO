---
layout: default
title: "Projects"
description: "LERO OSPO affiliated projects"
logo:
header-img:
ordernumber: 4
---

{% assign sorted_projects = site.projects | sort: "title" %}
<!--  {% assign today = "now" | date: "%d-%m-%Y" %} --> 

<section class="py-5">
  <div class="custom-container">
    <h2 class="mb-3 text-center">Projects</h2>
  </div>
  <div class="custom-container">
    <div class="row">
      {% for project in sorted_projects%}
          <div class="col-sm-12 col-md-6 col-lg-4 mb-4">
            {% if project.default_image %}
              <div class="card text-white card-has-bg click-col" style="background-image:url('/OSPO/img/projects/{{project.default_image}}');">
            {% else %}
              <div class="card text-white card-has-bg click-col" style="background-image:url('/OSPO/img/projects/default-img.png');">
            {% endif %}
            {% if project.url %}
              <a class="text-white" href="/OSPO{{project.url}}">
            {% endif %}
              <div class="card-img-overlay d-flex flex-column">
                <div class="card-body">
                  <h4 class="card-meta mb-2">{{project.name}}</h4>
                  <small class="card-title mt-0 "><p>{{project.short_description}}</p></small>
                </div>
              </div>
              </a>
            </div>
          </div>        
      {% endfor %}
    </div>
  </div>
</section>
