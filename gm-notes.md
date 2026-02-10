---
layout: page
title: GM Vault
description: Private GM notes and campaign resources
permalink: /gm-vault-32f8a9/
nav_exclude: true
---

# GM Vault – Campaign Resources

This page contains GM-only notes, planning documents, and hidden campaign information.

{% assign groups = site.gm | group_by: "topic" | sort: 'name' %}
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

**Quick Links:**
- [Campaign Planning](#)
- [Session Prep](#)
- [NPC Secrets](#)
- [Plot Threads](#)

*Remember: This URL is obscured but not secure. Don't post sensitive player information here.*
