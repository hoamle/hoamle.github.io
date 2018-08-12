---
layout: full-width
title: blog
# Note that this index page uses a full-width layout!
---

<h1 class="content-listing-header sans">Articles</h1>
I enjoy painting as much as I enjoy machine learning/AI. Therefore, the blog posts below are categorised accordingly to their intended audiences
><code>[T]</code> - scientific or technical posts
<br>
><code>[A]</code> - posts intended for (digital) artists
<br>
><code>no prefix</code> - posts for general audiences.

<ul class="content-listing ">
  {% for post in site.posts %}      
  <li class="listing">
    <hr class="slender">
    <a href="{{ post.url | prepend: site.baseurl }}">
      <body class="contrast">
        {% if {{post.category | number_of_words}} > 0 %}
        {% assign cat = {{post.category | upcase}} %}
        <code>[{{ cat | slice: 0 }}]</code>
        {% endif %}
        {{ post.title }}
      </body></a>
      <br><span class="smaller">{{ post.date | date: "%B %-d, %Y" }}</span>  <br/>
      <!-- <div>{{ post.excerpt }}</div>  -->
    </li>
    {% endfor %}
  </ul>