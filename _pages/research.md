---
layout: page
permalink: /research/
title: Research
description: Research themes and ongoing projects in the KOALA Lab.
nav: true
nav_order: 3
---

We develop learning and optimization methods that connect predictions to decisions,
working with NGOs and hospitals to address challenges in health and sustainability.

## Research Areas

<div class="projects">
  <div class="row row-cols-1 row-cols-md-2 row-cols-lg-3">
    {% assign sorted_projects = site.projects | sort: 'importance' %}
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
</div>

## Social Impact Applications

- **Pediatric care:** With Children’s Healthcare of Atlanta, we develop forecasting and early-warning tools to support clinical decisions and identify deterioration in hospitalized children.
- **Maternal and child health:** With [ARMMAN](https://www.armman.org/), we use decision-focused learning to improve service-call scheduling and engagement with mobile health information.
- **Migrant workers’ well-being:** With the Garden of Hope Foundation in Taiwan, we explore LLM-based conversational support through ongoing pilot studies.
- **Environmental sustainability:** With [Citizen of the Earth, Taiwan](https://www.cet-taiwan.org/), we use satellite imagery and AI to help identify illegal factory expansion.

[Learn more about our social impact work](https://guaguakai.com/impact).
