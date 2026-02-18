---
layout: page
title: PCs
description: Player character sheets and handouts
permalink: /pcs/
---

This section contains player-generated PDFs, grouped by topic. Each entry links to the embedded PDF for quick viewing.

You can update your character sheet by either:

- Modifying and re-uploading an identically-named PDF to the <a href="https://drive.google.com/drive/folders/1mKQR1Hvw9oPIOjnert72XOI3uB7LD0fI?usp=sharing">Google Drive</a>.
- Opening the PDF on Google Drive with Lumen PDF which allows in-place editing.

{% assign groups = site.pcs | group_by: "topic" | sort_natural: "name" %}

{% if groups.size > 0 %}
{% for group in groups %}

  {% if group.items.size > 0 %}
  <h2>{{ group.name }}</h2>
  <ul>
  {% assign items = group.items | sort: "title" %}
  {% for doc in items %}
    <li><a href="{{ doc.url | relative_url }}">{{ doc.title }}</a>{% if doc.summary %} — {{ doc.summary }}{% endif %}</li>
  {% endfor %}
  </ul>
  {% endif %}
{% endfor %}
{% else %}
<p><em>No PCs have been added yet.</em></p>
{% endif %}

---

*Ask the GM if you need to fully replace your PDF.*
