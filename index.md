---
layout: default
title: Home
---
{% assign numconference = 0 %}
        {% for conference in site.conferences %}
          {% assign numconference = numconference | plus: 1 %}
{% endfor %}

<h3>Improving Conferences: A database for scientific conferences and their key features</h3>
<hr>
<p> A list of {{ numconference }} national and international academic meetings in various disciplines for key features of inclusivity and sustainability and propose solutions to make conferences more modern, effective, equitable and intellectually productive for the research community and environmentally sustainable for our planet. </p>

<small>For more details pleace click the conference name.</small>

<table id='data_table' class="hover" style="width:100%">
  <thead>
  <tr>
    <th>Conference name</th>
    <th>Year</th>
    <th>Total years</th>
    <th>Discipline</th>
    <th>Gender Balance/Diversity Statement</th>
    <th>Attendance cost</th>
    <th>Registration fees</th>
    <th>Carbon footprint <small> (tons of CO<sub>2</sub>)</small></th>
    <th>Other carbon footprint <small>(tons of CO<sub>2</sub>)</small></th>

    <th>Society name</th>
    <th>Society members</th>
    <th>Attendees</th>
    <th>Venue</th>
    <th>Frequency</th>
    <th>Sponsors</th>
    <th>Virtual option</th>
    <th>Digital archives</th>
    <th>Electronic program dissemination</th>

    <th>On-site maternity</th>
    <th>On-site childcare</th>
    <th>Caregiver grant</th>
    <th>Career development</th>
    <th>ECR promotion events</th>
    <th>Travel awards</th>

     <th>Code of conduct</th>
     <th>Safety instructions</th>
     <th>Keynote speaker gender balance</th>
     <th>Speaker gender balance</th>
     <th>Invited speakers gender balance</th>
     <th>Session chair gender balance</th>
     <th>Conference chair gender balance</th>
     <th>Environmental sustainability</th>
     <th>Public engagement</th>
     <th>Sustainability initiatives</th>


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

  <td>{{ conference.society_name }}</td>
  <td>{{ conference.society_members }}</td>
  <td>{{ conference.attendees }}</td>
  <td>{{ conference.venue }}</td>
  <td>{{ conference.frequency }}</td>
  <td>{{ conference.sponsors }}</td>
  <td>{{ conference.virtual_option }}</td>
  <td>{{ conference.digital_archives }}</td>  
  <td>{{ conference.electronic_program }}</td>

  <td>{{ conference.onsite_maternity }}</td>
  <td>{{ conference.onsite_childcare }}</td>
  <td>{{ conference.caregiver_grant }}</td>
  <td>{{ conference.career_development }}</td>
  <td>{{ conference.ecr_promotion_events }}</td>
  <td>{{ conference.travel_awards }}</td>

  <td>{{ conference.code_of_conduct }}</td>
  <td>{{ conference.safety_instructions }}</td>
  <td>{{ conference.keynote_gender_balance }}</td>
  <td>{{ conference.speaker_gender_balance }}</td>
  <td>{{ conference.invited_gender_balance }}</td>
  <td>{{ conference.session_chair_gender_balance }}</td>
  <td>{{ conference.conference_chair_gender_balance }}</td>
  <td>{{ conference.environmental_sustainability }}</td>
  <td>{{ conference.public_engagement }}</td>
  <td>{{ conference.sustainability_initiatives }}</td>

  </tr>
{% endfor %}
  </tbody>
</table>

{% include footer.html %}
