---
title: Osteichthyes
layout: nav
permalink: /Osteichthyes/
---
<div id = "animal_os">
  {% assign sorted_exhibitosteichthyes = site.exhibitosteichthyes | sort: "title" %}
  {% for exhibitos in sorted_exhibitosteichthyes %}
    {% assign licence_url = site.data.licences | find: "licence", exhibitos.licence %}
    <div class = "grid_cell">
      <a href = "{{ exhibitos.url | relative_url }}"><img src="{{ exhibitos.image-url }}" class="gallery" width="450" height="400"></a >
      <p class = "caption"><a href = "{{ exhibitos.url | relative_url }}">{{ exhibitos.title }}</a ></p> 
      <p>by {{ exhibitos.creator }}</p>
      <p><a href="{{ licence_url.url }}">{{ exhibitos.licence }}</a ></p >
      <p>Tags: {{ exhibitos.tags }}</p >
    </div>
  {% endfor %}
</div>
<br>
<div class="attention">
 <p>* indicates that due to copyright or lack of resources, the image is not of the specific animal but of the family or genus to which it belongs, as indicated in the description page.</p>
 </div>