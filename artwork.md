---
layout: default
title: Sketch & Artwork
---
<div style="margin-top: 30px; text-align: center; margin-bottom: 30px">
		<!-- <div>
		<span style="font-size: 30px;">SCHAEDLER</span>
		</div> -->
		<span style="font-size: 23px; color: #888">SKETCHES AFTER THE MASTERS</span><br/>
		<span style="font-size: 18px; color: #aaa">
		Sketches in pencil, ink, and oil after the Old Masters
		</span>
</div>

{% for project in site.artworks | sort:"title" | reverse %}

{% if project.redirect %}
<div class="project">
    <div class="thumbnail">
        <a href="{{ project.redirect }}" target="_blank">
        {% if project.img %}
        <img class="thumbnail" src="{{ project.img }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ project.title }}</h1>
            <br/>
            <p>{{ project.description }}</p>
        </span>
        </a>
    </div>
</div>
{% else %}

<div class="project ">
    <div class="thumbnail">
        <a href="{{ site.baseurl }}{{ project.url }}">
        {% if project.img %}
        <img class="thumbnail" src="{{ project.img }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ project.title }}</h1>
            <br/>
            <p>{{ project.description }}</p>
        </span>
        </a>
    </div>
</div>

{% endif %}

{% endfor %}
