---
layout: default
title: "Resources"
description: "Lero OSPO research"
logo:
header-img: "img/home-bg.jpg"
ordernumber: 5
---

  <section class="py-5">
    <div class="custom-container">
      <h2 class="mb-3 text-center">Resources</h2> 
      <p class="text-justify">
        Lero researchers have a long history of contributing to Open Source research. One of the main goals of Lero OSPO is further promoting such research. A non-exhaustive list of research papers by Lero Researchers on different aspects of Open Source Software development and usage can be found below.
      </p>
    </div>
  </section>
<div class="custom-container">
  <ul class="resource">
    {% for resource in site.data.resources%}
      <li class="resource__item">
        <div class="name">{{resource.name}}</div>
        <a href="{{resource.file_url}}" class="btn btn-lero-outline" target="__blank">Download</a>
      </li>
    {% endfor %}
  </ul>
</div>
