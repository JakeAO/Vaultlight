---
layout: page
title: Sessions
description: Session summaries and campaign chronicle
permalink: /sessions/
---

Below are session summaries documenting the crew's exploits in Vaultlight, ordered chronologically.

{% assign items = site.sessions | sort: 'index' %}

{% if items.size > 0 %}
<ul>
{% for doc in items %}
  <li><a href="{{ doc.url | relative_url }}">{{ doc.title }}</a>{% if doc.summary %} — {{ doc.summary }}{% endif %}</li>
{% endfor %}
</ul>
{% else %}
<p><em>No sessions have been recorded yet. Check back after the first heist!</em></p>
{% endif %}

---

*Summaries are added after each session to track the crew's progress and decisions.*
