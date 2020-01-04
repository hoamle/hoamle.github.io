---
layout: default
title: About
priority: 80
---
<ul>
<li><h1 class="content-listing-header sans" style="text-align: center; opacity: 50%">Hoa M. Le</h1></li>
</ul>
<ul class="social-links">
  {% for entry in site.data.social %}
    <li>
      <a href="{{ entry.link }}"><span class="{{ entry.icon }}"></span></a>
    </li>
  {% endfor %}  
</ul>

{% marginfigure 'mf-id-1' 'assets/img/profile_2020.png' '' %}

I am currently the Data Science & AI Lead at [Pique.ai](//pique.ai/), working on recommender systems as both research engineer and analyst.

In my free time, I co-teach Deep learning foundation bootcamps at [VietAI](//vietai.org), sometimes <a href="/artwork">draw</a>, and have spent a little-too-much pondering over the advances of <a href="/blog/17/computers-can-draw">AI-assisted technology for creative works</a> which led to occasional <a href="/project">crossroads</a> with (deep) Generative models of images.

I graduated from <a href="//www.damtp.cam.ac.uk/">University of Cambridge</a> and <a href="//www.exeter.ac.uk/">University of Exeter</a> with a MPhil in Computational Biology and a BSc in Maths & Finance respectively. I then joined the <a href="//ds.soict.hust.edu.vn">Data Science Lab, Hanoi University of Science Technology</a>  as a Research Assistant, reading Statistical Machine Learning before moving to the industry. 
