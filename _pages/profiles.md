---
layout: profiles
permalink: /people/
title: people
description: Members of the Data Science lab @ MSU
nav: true
nav_order: 2

profiles:
  # if you want to include more than one profile, just replicate the following block
  # and create one content file for each profile inside _pages/
  - align: right
    image: AparnaLondon.jpg
    content: about_aparna.md
    image_circular: false # crops the image to make it circular
    category: faculty
    more_info: >
      <p>👩‍🏫: Dr. Aparna Varde</p>
      <p>📞: 973-655-4292</p>
      <p>📧: vardea@montclair.edu</p>
      <p>🏤: CCIS 111E </p>
    
  
  - align: right
    image: jiayinwang.jpg
    content: about_jiayin.md
    image_circular: false # crops the image to make it circular
    category: faculty
    more_info: >
      <p>👩‍🏫: Dr. Jiayin Wang</p>
      <p>📞: 973-655-3330</p>
      <p>📧: wangji@montclair.edu</p>
      <p>🏤: CCIS 227D </p>
  
  - align: right
    image: haoliu.jpg
    content: about_hao.md
    image_circular: false # crops the image to make it circular
    category: faculty
    more_info: >
      <p>👨‍🏫: Dr. Hao Liu</p>
      <p>📞: 973-655-4096</p>
      <p>📧: liuha@montclair.edu</p>
      <p>🏤: CCIS 227E </p>

  - align: right
    image: prof_pic_color.jpg
    content: about_hao.md
    image_circular: false # crops the image to make it circular
    category: student
    more_info: >
      <p>👨‍🏫: Hao Liu</p>
      <p>📞: 973-655-4096</p>
      <p>📧: liuha@montclair.edu</p>
      <p>🏤: CCIS 227E </p>
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
