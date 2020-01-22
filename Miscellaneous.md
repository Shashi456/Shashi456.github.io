---
layout: page
title: Miscellaneous 
permalink: /Miscellaneous/
---
While I research in deep learning, I've always been interested in learning more about everything. I'm interested in Venture capital, Personal Finance, cryptocurrencies, investing, microeconomics and lately have gotten into Mathematics and theoretical computer science (That's not much really). This section is mostly me writing about things i learn in those spaces or some retrospective thoughts on small experiments i try to conduct in my daily life.
<br class='brex'>

<!-- <h2>Mathematics</h2>
<section class="c-archives">
  <link rel="shortcut icon" href="">
  {% for post in site.tags.math  %}
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
-->

<h2>Computer Science (sans ML)</h2>
<section class="c-archives">
  <link rel="shortcut icon" href="">
  {% for post in site.tags.cs  %}
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

<h1> Economics and Finance</h1>
<h2>Valuation</h2>
One skill I've always wanted to pick up on has been Valuation. Now this could be the valuation of businesses, cryptocurrencies, assets or going a little bit far fetched, people. I've decided to learn through the Valuation course by
<a href="http://people.stern.nyu.edu/adamodar/">Aswath Damodaran</a>. 


<section class="c-archives">
  <link rel="shortcut icon" href="">
  {% for post in site.tags.valuation  %}
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

<h2>Microeconomics</h2>
I've always been interested in Microeconomics, it actually pops up everywhere in the modern world. One thing I think microeconomics teaches you is to think about problems within a framework while being wary about various variable and tradeoffs involved thereon.
 <!-- My first stop this year will be the course, MIT 14.01SC Principles of Microeconomics. One thing I aim to achieve by pursuing this course, is also observe how i learn and if MIT courses can be the first stop in Syllabus 2.0.
( Read <a href="https://danigrant.github.io/syllabus/">this</a> for more on syllabus 2.0, Thanks a lot to Dani Grant for the idea.) -->

  <link rel="shortcut icon" href="">
  {% for post in site.tags.me  %}
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

</section>
