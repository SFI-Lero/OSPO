---
layout: default
title: "Our Community"
description: "The LERO OSPO community"
logo:
header-img: "img/home-bg.jpg"
ordernumber: 2
---

{% assign sorted_people = site.data.people | sort:"order" %}

<section class="py-5">
  <div class="custom-container">
    <h2 class="mb-3 text-center">Mentors</h2> 
    <p class="text-justify">
      A mentor is someone who teaches or gives help and advice to a less experienced and often younger person. In an organizational setting, a mentor influences the personal and professional growth of a mentee.
    </p>
  </div>
</section>

<div class="container w-100 mb-4">
  <div class="member-block hor mx-auto">
    {% for people in sorted_people %} 
      {% if people.type == "mentor" and people.order == 1 %}
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
          <p> {{ people.interests }}</p>
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
        </div>
      {% endif %}
    {% endfor %}
  </div>
</div>
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
              <p> {{ people.interests }}</p>
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
            </div>
          </div>
        </div>
      {% endunless %}
    {% endfor %}
  </div>

</div>
