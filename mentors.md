---
layout: default
title: "Our Community"
description: "The LERO OSPO community"
logo:
header-img: "img/home-bg.jpg"
ordernumber: 2
---

{% assign sorted_people = site.mentors | sort: "lastname" %}

<section class="py-5">
  <div class="custom-container">
    <h2 class="mb-3 text-center">Director of Lero OSPO</h2> 
    <p class="text-justify text-center">
      The Director is in charge of determining the mission & vision of Lero OSPO.
    </p>
  </div>
</section>

<div class="container w-100 mb-4">
  <div class="member-block hor mx-auto">
    {% for people in sorted_people %} 
      {% if people.order == 1 %}
        <div class="member-info">
          {% if people.img %}
            <div class="pp small mb-2">
                <img class="profile_img" alt="" src="{{ site.baseurl }}/img/people/{{ people.img }}">
            </div>
          {% endif %}
          <h6>{{ people.lastname }}, {{ people.firstname }}</h6>
          <p>{{ people.role }}</p>
          <label class="text-secondary text-uppercase text-muted">{{ people.affiliation }}</label>
        </div>
        <div class="member-details fw">
          <p> {{ people.description }}</p>
          <div class="d-flex justify-content-between align-items-center bottom">
            <div class="d-flex mt-2">
              {% if people.email_address %}
                <a href="mailto:{{ people.email_address }}">
                  <div class="ic-box gh"><i class="bi bi-envelope-fill"></i></div>
                </a>
              {% endif %}
              {% if people.github_username %}
                <a href="https://github.com/{{ people.github_username }}" target="__blank">
                  <div class="ic-box gh"><i class="bi bi-github"></i></div>
                </a>
              {% endif %}
              {% if people.twitter_username %}
                  <a href="https://twitter.com/{{ people.twitter_username }}" target="__blank">
                    <div class="ic-box tw"><i class="bi bi-twitter"></i></div>
                  </a>
              {% endif %}
            </div>
            <a class="btn btn-lero-outline" href="/OSPO{{people.url}}">View more</a>
            <!-- <a class="btn btn-lero-outline" href="{{site.baseurl}}/Member_Detail/">View more</a> -->
          </div>
        </div>
      {% endif %}
    {% endfor %}
  </div>
</div>
<section class="py-5">
  <div class="custom-container">
    <h2 class="mb-3 text-center">Mentors</h2> 
    <p class="text-justify">
      The designated mentors of Lero OSPO are experienced in Open Source or Open Science and form the steering committee od OSPO.
      They are here to help all Lero members with their Open Science or Open Source activities.
    </p>
  </div>
</section>
<div class="container">
  <div class="row">
    {% for people in sorted_people %} 
      {% unless people.order == 1 %}
        <div class="col-md-3">
          <div class="member-block ver">
            <div class="member-info">
              {% if people.img %}
                <div class="pp small mb-2">
                    <img class="profile_img" alt="" src="{{ site.baseurl }}/img/people/{{ people.img }}">
                </div>
              {% endif %}
              <h6>{{ people.lastname }}, {{ people.firstname }}</h6>
              <p>{{ people.role }}</p>
              <label class="text-secondary text-uppercase text-muted">{{ people.affiliation }}</label>
            </div>
            <div class="member-details">
              <p> {{ people.description }}</p>
              <div class="d-flex justify-content-between align-items-center">
              <div class="d-flex mt-2">
                  {% if people.email_address %}
                    <a href="mailto:{{ people.email_address }}">
                      <div class="ic-box gh"><i class="bi bi-envelope-fill"></i></div>
                    </a>
                  {% endif %}
                  {% if people.github_username %}
                    <a href="https://github.com/{{ people.github_username }}" target="__blank">
                      <div class="ic-box gh"><i class="bi bi-github"></i></div>
                    </a>
                  {% endif %}
                  {% if people.twitter_username %}
                      <a href="https://twitter.com/{{ people.twitter_username }}" target="__blank">
                        <div class="ic-box tw"><i class="bi bi-twitter"></i></div>
                      </a>
                  {% endif %}
                </div>
                <a class="btn btn-lero-outline" href="/OSPO{{people.url}}">View more</a>
              </div>
            </div>
          </div>
        </div>
      {% endunless %}
    {% endfor %}
  </div>

</div>
