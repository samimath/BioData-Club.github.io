---
title: Lesson Material
layout: default
---

# Events/Workshops by Date

{% assign sorted_events = site.events | sort: 'date' | reverse %}
{% capture now_moment %}{{ "today" | date: '%s'}}{% endcapture %}

{% for event in sorted_events %}
    {% capture date %}{{ event.date | date: '%s'}}{% endcapture %}
     {% if date < now_moment and event.event_type == "workshop" %}
      {% include past_events.html %}
      {% endif %}
{% endfor %}

