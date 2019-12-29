---
layout: page
title: blog
# Note that this index page uses a full-width layout!
---
<br>
<!-- <h1 class="content-listing-header sans">Content</h1> -->
<ul class="content-listing ">
  {% for post in site.posts %}      
  <li class="listing">
    <hr class="slender">
    <a href="{{ post.url | prepend: site.baseurl }}">
      <body class="contrast">
        {{ post.title }}
      </body></a>
      {% if {{post.tag | size }} > 0 %}
      <br/>
      {% for cat in post.tag %}
      <span style="font-size: 12px; color: #666; text-transform: uppercase; margin-right: 2px">{{ cat }}</span>
      {% endfor %}
      {% endif %}
      <br><span class="smaller">{{ post.date | date: "%B %-d, %Y" }}</span>  <br/>
      <!-- <div>{{ post.excerpt }}</div>  -->
    </li>
    {% endfor %}
  </ul>