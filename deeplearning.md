---
layout: page
title: Deep Learning
permalink: /DL/
---
In reality, I'm learning to be a deep learning specialist. So under this section will be paper summaries/delving deep into the same. Notes for various courses I'm going to take throughout the year and finally some deep learning code I'll write. I'm extremely excited about the progress we are going to see in the next decade.

<h2>Courses</h2>
I've been pursuing a variety of courses over 2019, this section will mostly comrpise the notes i've made doing them.


<section class="c-archives">
  <link rel="shortcut icon" href="">
  {% for post in site.tags.DL  %}
  <ul class="c-archives__list">

    <li class="c-archives__item">
      <h3>
        <a href="{{ post.url | prepend: site.baseurl }}">{{post.title}}</a>
        <br>
        <small><p>{{post.description}}</p></small>
      </h3>
      <p>{{ post.date | date: "%b %-d, %Y" }}</p>
    </li>

  </ul>
  {% else %}
{% endfor %}
