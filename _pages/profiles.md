---
layout: profiles
permalink: /people/
title: people
description: members of the lab or group
nav: true
nav_order: 4

profiles:
  # if you want to include more than one profile, just replicate the following block
  # and create one content file for each profile inside _pages/
  - align: right
    image: AparnaLondon.jpg
    content: about_einstein.md
    image_circular: false # crops the image to make it circular
    more_info: >
      <p>👩‍🏫: Dr. Aparna Varde</p>
      <p>📞: 973-655-4292</p>
      <p>📧: vardea@montclair.edu</p>
      <p>🏤: CCIS 111E </p>
  - align: left
    image: prof_pic.jpg
    content: about_einstein.md
    image_circular: false # crops the image to make it circular
    more_info: >
      <p>Dr. xxx xxx</p>
      <p>555 your office number</p>
      <p>123 your address street</p>
      <p>Your City, State 12345</p>
---


## alumni

{% raw %}

```html

<div class="post">
{% for alum in site.data.alumni %}

<!-- The paddingtop and margin-top edits allow anchors to link properly. -->
<div id = "{{alum.name | replace: ' ', '-'}}" class="row" style="padding-top: 60px; margin-top: -60px; padding-bottom: 20px;">
  <strong>{{alum.name}}{% if alum.degrees %}, {{alum.degrees}} {% endif %}</strong> <br>
  <i>previously:</i> {{alum.previously}} <br>
  <i>now:</i> {{alum.now}}<br>
    {% if alum.website %} <i class="fa fa-globe"></i> <a href= "{{alum.website}}" target="_blank">{{alum.website}}</a>  {% endif %}
    {% for paper in site.data.publications %}
  {% if paper.authors contains alum.pubmed_name %}
  <div style="margin-left: 2.5em; padding-top: 8px; padding-bottom: 5px; ">{{paper.authors | remove: '*'}} <a href="/papers/index.html#{{paper.title | replace: ' ', '-' |  remove: '.'}}">{{paper.title}}</a> {{paper.details}}</div>
  {% endif %}
  {% endfor %}
</div>
{% endfor %}
</div>

```
{% endraw %}




## collaborators

{% raw %}
```html

<div class="post">
{% for collaborator in site.data.collaborators %}
<div id = "{{ collaborator.name | replace: ' ', '-' | remove: '.' }}" class="row" style="padding-top: 60px; margin-top: -60px; padding-bottom: 20px;">
<strong>{{collaborator.name}}{% if collaborator.degrees %}, {{collaborator.degrees}} {% endif %}</strong><br>  
  {{collaborator.position}}<br>
  {% if collaborator.website %} <i class="fa fa-globe"></i> <a href= "{{collaborator.website}}" target="_blank">{{collaborator.website}}</a>  {% endif %}
</div>
{% endfor %}
</div>

```
{% endraw %}
