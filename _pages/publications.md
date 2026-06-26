---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if site.author.googlescholar %}
  <div class="wordwrap">You can also find my articles on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</div>
{% endif %}

{% include base_path %}

{% assign publications = site.publications | where: "pub_group", "publication" %}
{% assign working_papers = site.publications | where: "pub_group", "working_paper" %}
{% assign dissertations = site.publications | where: "pub_group", "dissertation" %}

{% if publications.size > 0 %}
## Publications

{% for post in publications reversed %}
{% include archive-single.html %}
{% endfor %}
{% endif %}

{% if working_papers.size > 0 %}
## Working Papers

{% for post in working_papers reversed %}
{% include archive-single.html %}
{% endfor %}
{% endif %}

## Work in Progress

Bridging Inequality in Distance and Gender: Commuting and Child Penalty in the Austrian Labor Market. Funded by the Austrian Academy of Sciences.

{% if dissertations.size > 0 %}
## Dissertation

{% for post in dissertations reversed %}
{% include archive-single.html %}
{% endfor %}
{% endif %}
