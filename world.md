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
  {% if group.name == "NPCs" %}
  {% assign npc_groups = group.items | group_by: "affiliation" | sort: 'name' %}
  <ul>
  {% for npc_group in npc_groups %}
    {% assign affiliation_name = npc_group.name %}
    {% if affiliation_name == "" %}
      {% assign affiliation_name = "Unaffiliated" %}
    {% endif %}
    <li>{{ affiliation_name }}
      <ul>
      {% assign npc_items = npc_group.items | sort: 'title' %}
      {% for doc in npc_items %}
        <li><a href="{{ doc.url | relative_url }}">{{ doc.title }}</a>{% if doc.summary %} — {{ doc.summary }}{% endif %}</li>
      {% endfor %}
      </ul>
    </li>
  {% endfor %}
  </ul>
  {% else %}
  <ul>
  {% assign items = group.items | sort: 'title' %}
  {% for doc in items %}
    <li><a href="{{ doc.url | relative_url }}">{{ doc.title }}</a>{% if doc.summary %} — {{ doc.summary }}{% endif %}</li>
  {% endfor %}
  </ul>
  {% endif %}
  {% endif %}
{% endfor %}

---

*This section grows as the crew explores the city and uncovers its secrets.*
