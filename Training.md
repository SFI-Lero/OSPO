---
layout: default
title: "Training and Resources"
description: "The LERO OSPO community"
logo:
header-img:
ordernumber:
---


{%assign sorted_events = site.data.events | sort: "events" %}

# Events

<html>
<div class="row">

{% for events in sorted_events%} 
    {{ events.name }}
    {{ events.location }}
{% endfor %}
</div>
</html>

