---
layout: page
title: Money Matters
permalink: /Moneymatters/
---
Money matters, i don't mean it in the money is important sense but more like different matters of money. I'm interested in Venture capital, Personal Finance, cryptocurrencies and investing and microeconomics (That's not much really). This section is mostly me writing about things i learn in that space or some retrospective thoughts on small experiments i try to conduct in my daily life.
<br class='brex'>

<h2>Valuation</h2>
One skill I've always wanted to pick up on has been Valuation. Now this could be the valuation of businesses, cryptocurrencies, assets or going a little bit far fetched, people. This year in 2019, I've decided to take the Valuation course by [Aswath Damodaran](http://people.stern.nyu.edu/adamodar/). He offers the same course to both Undergrads and MBA students, I don't think I will find better resources for the same. I aim to write notes for the class under this tab, also trying to do assignments and other challenges given in the class.


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
