---
layout: default
---

# Linux User Group

What can we do for UCL to adopt Linux more broadly? In these pages you'll find our efforts to find that out.

We are a group of prole from different departments at UCL, some of us are from [UCL's Advanced Research Computing Centre](https://ucl.ac.uk/arc) (ARC), others from [Digital Education](https://blogs.ucl.ac.uk/digital-education/), but we are not alone. Check our [about page]({{ 'about.html' | relative_url }}) to find out who we are.

In these pages you will find:

- Announcements of [Activities & events](./events) that are happening in UCL (or near by) related to Linux.
- [News](./news) related to Linux that is of interest to the UCL community.
- A number of [Guides](./guides) that you may find useful.

Our announcements and news page provide an <i class="fa-solid fa-rss"></i> [RSS feed]({{"feed.xml" | prepend: baseurl}}) so you can be up to date without having to visit our page all the time, and the listed events are also available on our [published calendar](https://outlook.office365.com/owa/calendar/30254fbb15664ffaad6db9083612c8fc@ucl.ac.uk/c694a042ffa7448583f74810d8fba9a317208102663315025766/calendar.ics).

## Latest News <a href="{{'feed.xml' | prepend: baseurl}}"> <span class="icon-image  icon--github"> <svg viewBox="0 0 16 16"> <path fill="#000000" d="{{ site.data.icons.rss_logo }}"/> </svg> </span></a>

<!-- List of latest 5 news articles -->

{% for item in site.posts limit:5 %} <!-- site.posts is already sorted -->
- 📆 {{item.date | date: "%Y-%m-%d"}} - [{{item.title}}]({{item.url | prepend: site.baseurl }})
{% endfor %}

## Upcoming events [🗓️](https://outlook.office365.com/owa/calendar/30254fbb15664ffaad6db9083612c8fc@ucl.ac.uk/c694a042ffa7448583f74810d8fba9a317208102663315025766/calendar.ics)

{% capture nowunix %}{{ 'now' | date: '%s' }}{% endcapture %}
{% assign doclist =  site.data.events | sort: 'date' %}
{% for event in doclist %}
{%- capture event_date -%}{{event.date | date: '%s'}}{%- endcapture -%}
{% if event_date >= nowunix %}

- 📆 {{event.date | date: "%Y-%m-%d"}} - [{{event.title}}]({{event.url}}) (by {{event.organiser}})
  {%- endif -%}
  {% endfor %}
