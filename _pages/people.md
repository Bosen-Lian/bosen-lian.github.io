---
layout: page
permalink: /people
title: Team
description: 
nav: true
nav_order: 6
nav_rank: 3
---

<style>
.post-title, .page-title { font-weight: 700 !important; }
</style>


{% assign groups = site.people | sort: "group_rank" | map: "group" | uniq %}
{% for group in groups %}
<h2 style="font-weight: 700; margin-top: 2rem;">{{ group }}</h2>

    {% assign members = site.people | sort: "lastname" | where: "group", group %}
    {% for member in members %}
<p>
    <div class="card {% if member.inline == false %}hoverable{% endif %}">
        <div class="row no-gutters">
            <div class="col-sm-4 col-md-3">
            	{% if member.inline == false %}<a href="{{ member.url | relative_url }}">{% endif %}
                <img src="{{ '/assets/img/' | append: member.profile.image | relative_url }}" class="card-img img-fluid" alt="{{ member.profile.name }}" />
            	{% if member.inline == false %}</a>{% endif %}
            </div>
            <div class="team col-sm-8 col-md-9">
                <div class="card-body">
                    {% if member.inline == false %}<a href="{{ member.url | relative_url }}">{% endif %}
                    <h5 class="card-title">{{ member.profile.name }}</h5>
                    {% if member.profile.position %}<h6 class="card-subtitle mb-2 text-muted">{{ member.profile.position }}</h6>{% endif %}
                    <p class="card-text">
                        {{ member.teaser }}
                    </p>
                    {% if member.inline == false %}</a>{% endif %}
                    {% if member.profile.email %}
                        <a href="mailto:{{ member.profile.email }}" class="card-link"><i class="fas fa-envelope"></i></a>
                    {% endif %}
                    {% if member.profile.phone %}
                        <a href="tel:{{ member.profile.phone }}" class="card-link"><i class="fas fa-phone"></i></a>
                    {% endif %}
                    {% if member.profile.orcid %}
                        <a href="https://orcid.org/{{ site.orcid_id }}" title="ORCID"><i class="ai ai-orcid"></i></a>
                    {% endif %}
                    {% if member.profile.scholar_userid %}
                        <a href="https://scholar.google.com/citations?user={{ site.scholar_userid }}" title="Google Scholar"><i class="ai ai-google-scholar"></i></a>
                    {% endif %}
                    {% if member.profile.twitter %}
                        <a href="https://twitter.com/{{ member.profile.twitter }}" class="card-link" target="_blank"><i class="fab fa-twitter"></i></a>
                    {% endif %}
                    {% if member.profile.github %}
                        <a href="https://github.com/{{ member.profile.github }}" class="card-link" target="_blank"><i class="fab fa-github"></i></a>
                    {% endif %}
                    {% if member.profile.website %}
                        <a href="{{ member.profile.website }}" class="card-link" target="_blank"><i class="fas fa-globe"></i></a>
                    {% endif %}
                    <p class="card-text">
                        <small class="test-muted"><i class="fas fa-thumbtack"></i> {{ member.profile.address | replace: '<br />', ', ' }}</small>
                    </p>
                </div>
            </div>
        </div>
    </div>
</p>
    {% endfor %}
{% endfor %}



<!--
## Undergraduate Students

- **Camille Campbell** — Department of Electrical and Computer Engineering, Auburn University, 2023–2028.
- **Colin Bucey** — Department of Electrical and Computer Engineering, Auburn University, 2023–2027.
- **Logan A. Green** — Research Intern, 2024–2028; Department of Electrical and Computer Engineering, University of Florida.
-->

---

## **Alumni**

- **Yifan Zhang** — M.S. Student, 2023–2025. Now a Ph.D. student in the Department of Computer Science and Software Engineering, Auburn University.
- **Nik Kandula** — Undergraduate Researcher, Summer 2025. Now an undergraduate student in the Department of Electrical and Computer Engineering, Auburn University.
- **James Byard** — Undergraduate Researcher, Summer 2025. Now an undergraduate student in the Department of Electrical and Computer Engineering, Auburn University.

---

## **Academic Family Tree**

Our academic lineage traces back through generations of mathematicians and scientists — from Galileo, Huygens, and the Bernoullis through Euler, Lagrange, Fourier, and Dirichlet — to the present-day lab.

<img src="{{ '/assets/img/researchfamilytree.png' | relative_url }}" class="img-fluid rounded z-depth-1" alt="Academic family tree tracing the lab's research lineage from Galileo to the present">


---

Copyright © 2026 Bosen Lian. All rights reserved.







