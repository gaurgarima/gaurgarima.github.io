---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Education
======
* PhD (with MTech), Computer Science and Engineering, IIT Kanpur, 2021
* BE, Information Technology, Madhav Institute of Technology and Science, Gwalior, 2013

Research Positions
======
* Since Feb 2024: Postdoctoral Researcher, CEDAR team, Inria Saclay
* Mar 2022 to Dec 2023: Postdoctoral Researcher, IIT Delhi
* Jan 2021 to Mar 2022: Research Scientist, IIT Delhi
* 2016: Summer Intern, IBM Research Delhi

Publications
======
<ul>{% for post in site.publications reversed %}
  {% include archive-single-cv.html %}
{% endfor %}</ul>

Teaching
======
<ul>{% for post in site.teaching reversed %}
  {% include archive-single-cv.html %}
{% endfor %}</ul>

Talks and Demos
======
<ul>{% for post in site.talks reversed %}
  {% include archive-single-talk-cv.html %}
{% endfor %}</ul>

Tools and Repositories
======
* FactCheckBureau (CIKM 2024 demo): [Tool record](https://zenodo.org/records/13868429), [Code repository](https://gitlab.inria.fr/cedar/factcheckbureau), [Dataset record](https://zenodo.org/records/13898319)

Mentoring
======
* M1 and M2 interns at Inria/École Polytechnique/Telecom Paris across projects in fact-check retrieval, named-entity-centric data cleaning, and heterogeneous data querying.

References
======
* Ioana Manolescu, Inria Saclay
* Srikanta Bedathur, IIT Delhi
* Arnab Bhattacharya, IIT Kanpur
