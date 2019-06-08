---
layout: page
title: My Musings
permalink: /musings/
---
My thoughts and ideas, I sporadically sometimes muse about things depending on my mood or just some random epiphanies i have throughout the day. These thoughts are purely my own and i'd love to talk about them.

***

<section class="c-archives">
  <link rel="shortcut icon" href="">
  {% for post in site.tags.rfs  %}
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


***

<br class= 'brex'>
<section class="c-archives">
  <link rel="shortcut icon" href="">
  {% for post in site.tags.personal  %}
  <!-- {% capture this_year %}{{ post.date | date: "%Y" }}{% endcapture %}
  {% capture next_year %}{{ post.previous.date | date: "%Y" }}{% endcapture %} -->
  {% if forloop.first %}
  <!-- <h2 class="c-archives__year" id="{{ this_year }}-ref">{{this_year}}</h2> -->
  <h2>Personal Thoughts</h2>
  <ul class="c-archives__list">
    {% endif %}
    <li class="c-archives__item">
      <h3>
        <a href="{{ post.url | prepend: site.baseurl }}">{{post.title}}</a>
        <br>
        <small><p>{{post.description}}</p></small>
      </h3>
      <p>{{ post.date | date: "%b %-d, %Y" }}</p>
    </li>
    {% if forloop.last %}
  </ul>
  {% else %}
  {% if this_year != next_year %}
</ul>
<h2 class="c-archives__year" id="{{ next_year }}-ref">{{next_year}}</h2>
<ul class="c-archives__list">
  {% endif %}
  {% endif %}
  {% endfor %}

<h2>Ideas</h2>
  <link rel="shortcut icon" href="">
  {% for post in site.tags.ideas  %}

  <ul class="c-archives__list">

    <li class="c-archives__item">
      <h3>
        <a href="{{ post.url | prepend: site.baseurl }}">{{post.title}}</a>
        <br>
        <small><p>{{post.description}}</p></small>
      </h3>
      <p>{{ post.date | date: "%b %-d, %Y" }}</p>
    </li>
    {% if forloop.last %}
  </ul>
  {% else %}
  {% if this_year != next_year %}
</ul>
<h2 class="c-archives__year" id="{{ next_year }}-ref">{{next_year}}</h2>
<ul class="c-archives__list">
  {% endif %}
  {% endif %}
  {% endfor %}

</section>
