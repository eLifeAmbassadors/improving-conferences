---
layout: page
title: Conferences by Discipline
---

{% comment %}
Code adapted from
https://codinfox.github.io/dev/2015/03/06/use-tags-and-categories-in-your-jekyll-based-github-pages/
{% endcomment %}

{% comment %}
=========================================
Collect and sort disciplines and display tags
=========================================
{% endcomment %}

{% assign disciplines = "" %}
{% for conference in site.conferences %}
    {% assign discipline = conference.funder | append: ' - ' %}
    {% if conference.discipline != nil %}
        {% assign discipline = discipline | append: conference.discipline | join:'|' | append:'|' %}
    {% else %}
        {% assign discipline = discipline | append: '(N/A)' | join:'|' | append:'|' %}
    {% endif %}
	{% unless disciplines contains discipline %}
        {% assign disciplines = disciplines | append:discipline %}
	{% endunless %}
{% endfor %}
{% assign disciplines = disciplines | split:'|' | sort %}

<p>
{% for discipline in disciplines %}
	<a href="#{{ discipline | slugify }}" class="post-tag">{{ discipline }}</a>
{% endfor %}
</p>


{% comment %}
=========================
List all conferences by discipline
=========================
{% endcomment %}

<p>
{% for discipline in disciplines %}
	<h3 id="{{ discipline | slugify }}">{{ discipline }}</h3>
	<ul>
	 {% for conference in site.conferences %}
         {% assign mydiscipline = conference.funder | append: ' - ' %}
         {% if conference.discipline != nil %}
            {% assign mydiscipline = mydiscipline | append: conference.discipline %}
         {% else %}
            {% assign mydiscipline = mydiscipline | append: '(N/A)' %}
         {% endif %}
		 {% if mydiscipline == discipline %}
		 <li>
		 <a href="{{ conference.url }}">
		 {{ conference.name }}
		 </a>
 		 <small>{{ conference.year }}, <em>{{ conference.venues }}</em></small>
		 </li>
		 {% endif %}
	 {% endfor %}
	</ul>
{% endfor %}
</p>
