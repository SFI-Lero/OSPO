---
layout: pagefullwidth
title: "People"
description: "Members and researchers of BioMEC"
logo:
header-img: "img/home-bg.jpg"
ordernumber: 3
---

<!--This file renders the people page. Normal markdown is used at the top and for headings. The actual people set is rendered using HTML to enable responsive rendering-->


---



<html>

<div class="row">
	<!--Using LIQUID to code adding of people-->
	{% assign sorted_people = site.data.people | sort:"name" %}
	{% for people in sorted_people %}

	<div class="col-xs-12 col-sm-6 col-md-4 col-lg-3"> <!--Reforms array of people, full width=12-->
	<!--Include HTML file for rendering person-->
		{% include addPerson.html people=site.data.people %}
	</div>

	{% endfor %}
</div>
</html>
