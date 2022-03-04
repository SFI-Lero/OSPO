---
layout: pagefullwidth
title: "People"
description: "The LERO OSPO community"
logo:
header-img: "img/home-bg.jpg"
ordernumber: 2
---

<!--This file renders the people page. Normal markdown is used at the top and for headings. The actual people set is rendered using HTML to enable responsive rendering-->


---





{% assign sorted_people = site.data.people | sort:"name" %}

# Mentors
<html>
<div class="row">

{% for people in sorted_people %} {% if people.type == "mentor" %}
	<div class="col-xs-12 col-sm-4 col-md-3 col-lg-3">
		{% include addPerson.html people=site.data.people %}
	</div>
{% endif %}{% endfor %}

</div>
</html>

# Members
<html>
<div class="row">

{% for people in sorted_people %} {% if people.type == "member" %}
	<div class="col-xs-12 col-sm-4 col-md-3 col-lg-3">
		{% include addPerson.html people=site.data.people %}
	</div>
{% endif %}{% endfor %}

</div>
</html>
