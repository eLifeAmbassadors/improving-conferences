---
layout: page
title: Contribute
---

## Add/edit using GitHub

If you're familiar with GitHub you can submit a pull request to add conference to the web site (or open an issue with the necessary information).

### Conference information

Information for each conference is stored as YAML with fields for each key piece of information.

```markdown
---
layout: conference 
name: 'IVBM meeting'
year: '2018'
discipline: 'Vascular Biology'
total_years: '20'
society_name: 'North American Vascular Biology Organization (NAVBO)'
society_members: ''
attendees: ''
venue: 'Helsinki, Finland'
frequency: 'Biennial'
sponsors: ''
virtual_option: 'None'
digital_archives: 'None'
attendance_cost: ' $2000-$4000'
registration_fee: '$250-$600'
carbon_footprint: '0'
other_carbon_footprint: '0'
electronic_program: 'Yes the program was provided online on conference website.'
onsite_maternity: 'None'
onsite_childcare: 'None'
caregiver_grant: 'None'
career_development: 'None'
ecr_promotion_events: 'NONE'
travel_awards: 'Yes a limited number for Under 45 years old - International participants - Presenting author who are from (China / Japan, Southeast / Middle Asia, The Americas / Europe / Oceania / Africa)'
code_of_conduct: 'None'
safety_instructions: 'None'
gender_balance: 'None'
keynote_gender_balance: ''
speaker_gender_balance: ''
invited_gender_balance: ''
session_chair_gender_balance: ''
conference_chair_gender_balance: '2 WOMEN: 4 MEN'
environmental_sustainability: 'None'
public_engagement: 'None'
sustainability_initiatives: 'None'
conference_url: 'http://research.med.helsinki.fi/cancerbio/IVBM/'
other_details: ''
---
```

The items to the right of the `:` on each line should be changed to match the conference you want to add.

You can submit a pull request that adds the above information to a file named `conference_name_year.md` in the `_conferences` folder of the [GitHub repository]({{ site.github.repo }}).

Or just [open an issue](https://github.com/eLifeAmbassadors/improving-conferences/issues/new) and paste the filled out YAML into that issue.

