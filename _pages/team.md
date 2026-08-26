---
layout: single
title: "Team Members"
permalink: /team/
author_profile: false
toc: false
---

SLICE brings together researchers across institutions in Europe, North
America, and the Middle East.

{% for group in site.data.team %}
## {{ group.label }}

<div class="team-grid">
{% for person in group.people %}{% include team-card.html person=person %}{% endfor %}
</div>
{% endfor %}
