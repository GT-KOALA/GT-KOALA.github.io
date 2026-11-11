---
layout: page
permalink: /team/
title: Team
description: Members of the KOALA Lab at Georgia Tech.
nav: true
nav_order: 2
---

<div class="team-page">
  <p class="team-intro">Meet the people developing learning and optimization methods for real-world social impact.</p>

  <section class="team-lead" aria-labelledby="team-lead-heading">
    <a href="https://guaguakai.com/" class="team-lead-photo" aria-label="Kai Wang's personal website">
      <img src="{{ '/assets/img/team/kai-wang.jpg' | relative_url }}" alt="Kai Wang">
    </a>
    <div>
      <h2 id="team-lead-heading"><a href="https://guaguakai.com/">Kai Wang</a></h2>
      <p>Principal Investigator · Assistant Professor</p>
      <p class="team-meta">School of Computational Science and Engineering, Georgia Tech<br>
      <a href="mailto:kaiwang.gua@gmail.com">kaiwang.gua@gmail.com</a> · CODA S1309</p>
    </div>
  </section>

{% for group in site.data.team %}
<section class="team-section" aria-labelledby="team-{{ group.title | slugify }}">
<div class="team-section-heading">
<h2 id="team-{{ group.title | slugify }}">{{ group.title }}</h2>
<span class="team-count">{{ group.members.size }}</span>
</div>
<div class="team-grid">
{% for member in group.members %}
{% include team_member.liquid member=member %}
{% endfor %}
</div>
</section>
{% endfor %}
</div>

## Join Us

We will recruit **1–2 PhD students** for **Fall 2027** — prospective students are welcome to apply through the
[Georgia Tech CSE PhD program](https://cse.gatech.edu/academics/phd) and reach out by email.

MS/BS students at Georgia Tech are welcome to take our courses (CSE/ISyE 6740, CSE 8803)
and reach out afterward. We have limited research capacity for non-PhD students.

Prospective PhD students should list Kai Wang in their application and select the
CS, ML, or CSE track in the School of CSE. When emailing, describe how your research
interests overlap with the lab’s work. See the
[prospective-student guidance](https://guaguakai.com/team) for additional details.
