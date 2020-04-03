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
name: 'International Conference on Community Ecology'
year: '2019'
discipline: 'Ecology'
total_years: '2'
society_name: 'Not Applicable'
society_members: 'Not Applicable'
attendees: '200'
venue: 'Bologna, Italy'
frequency: 'Annual'
sponsors: 'Center for Ecological Research (Hungarian Academy of Scinece), Universitat di Bologna'
virtual_option: 'None'
digital_archives: 'None'
attendance_cost: ' $2000-$4000'
registration_fee: 'No information available'
carbon_footprint: '300'
other_carbon_footprint: '60'
electonic_program: 'Yes - Program book and Abstract book were both provided on the conference website.'
onsite_maternity: 'None'
onsite_childcare: 'None'
caregiver_grant: 'None'
career_development: 'None'
ecr_promotion_events: 'None'
travel_awards: 'None'
code_of_conduct: 'None'
code_of_ethics: ''
safety_instructions: 'None'
gender_balance: 'None'
keynote_gender_balance: 'None'
speaker_gender_balance: '4 Men: 2 Women'
invited_gender_balance: 'No information available'
session_chair_gender_balance: 'No Information available'
conference_chair_gender_balance: 'Organizers: 3 Men: 2 Women, Conf chair: 1 Man'
environmental_sustainability: 'None'
public_engagement: 'None'
sustainability_initiatives: 'None'
conference_url: 'https://confcomec.akcongress.com/'
other_details: ''
---
```

The items to the right of the `:` on each line should be changed to match the conference you want to add.

You can submit a pull request that adds the above information to a file named `conference_name_year.md` in the `_conferences` folder of the [GitHub repository]({{ site.github.repo }}).

Or just [open an issue](https://github.com/eLifeAmbassadors/improving-conferences/issues/new) and paste the filled out YAML into that issue.

