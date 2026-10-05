---
title: "US Immigration History"
layout: base
date: 2026-10-13
header-image: "/assets/images/immigration_collage.jpg"
header-title: Family Migration Stories 
header-subtitle: US Immigration History 2H Fall 2026 
header-position: 35% center
---

#Family Migration Stories

For US Immigration History, students have collected oral histories about their families' migration stories. Using a template inspired by the University of Minnesota's Immigration History Research Center's Immigration Stories project, students have drawn on class themes and additional research to tell their family's migration stories. 



The card grid below links to the sample essays. The info on these cards come from the essay pages themselves. As students publish their essaysm, these will showcase students' work as the project develops.

{% assign all_pages = site.pages %}
{% assign cards = all_pages | where_exp: "p", "p.path contains 'essays/'" | where_exp: "p", "p.path != 'essays/index.md'" %}

{% include cards/card-grid.html cards=cards %}

