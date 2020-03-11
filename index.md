---
layout: default
title: Home
---

{% assign numconference = 0 %}
{% for conference in site.conferences %}
  {% assign numconference = numconference | plus: 1 %}
{% endfor %}
<h3>A database of scientific conferences and its key features</h3>

A list of {{ numconference }} national and international academic meetings in various disciplines for key features of inclusivity and sustainability and propose solutions to make conferences more modern, effective, equitable and intellectually productive for the research community and environmentally sustainable for our planet. 

<table id='data_table' class="hover" style="width:100%">
  <thead>
  <tr>
    <th>Conference</th>
    <th>Year</th>
    <th>Discipline</th>
    <th>Gender Balance</th>
    <th>Carbon footprint</th>
  </tr>
  </thead>

  <tbody>
{% for conference in site.conferences %}
  <tr>
	<td><a href="{{ site.baseurl }}{{ conference.url }}">{{ conference.name }}</a></td>
  <td>{{ conference.year }}</td>
  <td>{{ conference.discipline }}</td>
	<td>{{ conference.gender_balance }}</td>
  <td>{{ conference.carbon_footprint }}</td>
  </tr>
{% endfor %}
  </tbody>
</table>

{% include footer.html %}
