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

<small>For more details pleace click the conference name.</small>

<table id='data_table' class="hover" style="width:100%">
  <thead>
  <tr>
    <th>Conference name</th>
    <th>Year</th>
    <th>Total years</th>
    <th>Discipline</th>
    <th>Gender Balance</th>
    <th>Attendance cost</th>
    <th>Registration fees</th>
    <th>Carbon footprint</th>
    <th>Other carbon footprint</th>
    <th>On-site maternity</th>
    <th>On-site childcare</th>
    <th>Caregiver grant</th>
    <th>Career development</th>
    <th>ECR promotion events</th>
    <th>Travel awards</th>
  </tr>
  </thead>

  <tbody>
{% for conference in site.conferences %}
  <tr>
	<td><a href="{{ site.baseurl }}{{ conference.url }}">{{ conference.name }}</a></td>
  <td>{{ conference.year }}</td>
  <td>{{ conference.total_years }}</td>
  <td>{{ conference.discipline }}</td>
	<td>{{ conference.gender_balance }}</td>
  <td>{{ conference.attendance_cost }}</td>
  <td>{{ conference.registration_fee }}</td>
  <td>{{ conference.carbon_footprint }}</td>
  <td>{{ conference.other_carbon_footprint }}</td>
  <td>{{ conference.onsite_maternity }}</td>
  <td>{{ conference.onsite_childcare }}</td>
  <td>{{ conference.caregiver_grant }}</td>
  <td>{{ conference.career_development }}</td>
  <td>{{ conference.ecr_promotion_events }}</td>
  <td>{{ conference.travel_awards }}</td>

  </tr>
{% endfor %}
  </tbody>
</table>

{% include footer.html %}
