---
title: Online Hosted Instructions
permalink: index.html
layout: home
---

# Content Directory

Hyperlinks to each of the lab exercises and demos are listed below.

## Labs

{% assign labs = site.pages | where_exp:"page", "page.url contains '/Instructions/Labs'" %}
| Module | Exercises |
| --- | --- | 
{% for activity in labs  %}| {{ activity.lab.module }} | [{{ activity.lab.title }}]({{ site.github.url }}{{ activity.url }}) |
{% endfor %}

## Demonstrations

{% assign demos = site.pages | where_exp:"page", "page.url contains '/Instructions/Demos'" %}
| Module | Demos |
| --- | --- | 
{% for activity in demos  %}| {{ activity.demo.module }} | [{{ activity.demo.title }}]({{ site.github.url }}{{ activity.url }}) |
{% endfor %}
