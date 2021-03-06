---
title: Workshop and Discussion Materials
layout: single
toc: true
---
Here are past discussion topics and workshops from BioData Club, sorted by the date they were given. Where possible, we have linked to recordings, presentations, and code.

{% assign sorted_events = site.events | sort: 'date' | reverse %}
{% capture now_moment %}{{ "today" | date: '%s'}}{% endcapture %}

{% for event in sorted_events %}
    {% capture date %}{{ event.date | date: '%s'}}{% endcapture %}
     {% if date < now_moment and event.event_type == "workshop" %}
      {% include past_events.html %}
      {% endif %}
{% endfor %}

# Educational Resources

## [R-Bootcamp](https://r-bootcamp.netlify.com)

This was a four part course that is free that introduces everyone to visualizing, data wrangling, and simple statistics with `tidyverse` packages.

# Discussion Topics

This is a list of discussion topics and talks hosted by BioData Club that we think have been successful and may be of interest

+ [Good Enough Practices For Scientific Computing](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1005510) 
  
This is a paper by Greg Wilson that outlines how to improve your scientific software.

+ [How to Be a Modern Scientist](https://www.scribd.com/document/325829082/Modern-Scientist) 

We had a discussion about Jeff Leek's book *How to be a Modern Scientist* and what it means for students and postdocs today. 

+ [Take a Sad Plot and Make it Better: A Case Study with R and ggplot2](https://apreshill.github.io/ohsu-biodatavis/slides.html) 
  
Alison Presmanes Hill gave a talk for our visualization hacky hour about how she slowly revised and improved a figure. Very funny and very informative.

+ [Ten Simple rules for a Successful Cross-Disciplinary Collaboration](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1004214)

We at BioData Club are cross-disciplinary by nature. What does it take to be a good cross-disciplinary collaborator?

