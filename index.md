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

I am a Full-stack AI engineer, currently titled Senior Data Scientist at [Momo](//crunchbase.com/organization/momo-vn) - who had acquired [Pique.ai](//pique.ai/) where I was the Data Science & AI Lead.

I graduated from <a href="//www.damtp.cam.ac.uk/">University of Cambridge</a> and <a href="//www.exeter.ac.uk/">University of Exeter</a>, with degrees in Computational Biology, Maths and Finance. I then joined <a href="http://ds.soict.hust.edu.vn">Data Science Lab, Hanoi University of Science & Tech</a> as a Research Assistant, reading Statistical Machine Learning before moving to the industry. 

In my free time, I <a href="/art">draw</a> sometimes, used to teach Deep Learning bootcamps at [VietAI](//vietai.org/our-program/), and have been exploring the use of <a href="/portfolio#compart">AI technologies for creative works</a> over the years.
