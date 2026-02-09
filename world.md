---
layout: page
title: World
description: Setting, characters, locations, and lore revealed during play
permalink: /world/
---

This page contains all player-facing information about the world of Vaultlight – the city, its inhabitants, key locations, and the cosmic mysteries lurking in the shadows.

Information is added here as it's discovered during the campaign.

{% assign groups = site.world | group_by: "topic" | sort: 'name' %}
{% for group in groups %}

  {% if group.items.size > 0 %}
  <h2>{{ group.name }}</h2>
  <ul>
  {% assign items = group.items | sort: 'title' %}
  {% for doc in items %}
    <li><a href="{{ doc.url | relative_url }}">{{ doc.title }}</a>{% if doc.summary %} — {{ doc.summary }}{% endif %}</li>
  {% endfor %}
  </ul>
  {% endif %}
{% endfor %}

---

*This section grows as the crew explores the city and uncovers its secrets.*
