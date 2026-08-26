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
{% for person in group.people %}
  <div class="team-card">
    {% if person.image %}
      <img src="{{ person.image | relative_url }}" alt="{{ person.name }}" class="team-photo">
    {% else %}
      <div class="team-photo team-photo--placeholder">
        <span>{{ person.name | split: " " | first | slice: 0 }}{{ person.name | split: " " | last | slice: 0 }}</span>
      </div>
    {% endif %}
    <div class="team-info">
      {% if person.url %}
        <p class="team-name"><a href="{{ person.url }}">{{ person.name }}</a></p>
      {% else %}
        <p class="team-name">{{ person.name }}</p>
      {% endif %}
      {% if person.role %}<p class="team-role">{{ person.role }}</p>{% endif %}
      {% if person.institution %}<p class="team-inst">{{ person.institution }}</p>{% endif %}
    </div>
  </div>
{% endfor %}
</div>
{% endfor %}
