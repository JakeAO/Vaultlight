---
layout: page
title: Rules & Info
description: FATE Condensed rules, mechanics, and cheat sheets
permalink: /info/
---

This page contains player-facing rules clarifications, cheat sheets, and game mechanics for the Vaultlight campaign.

## Core Resources

- **[FATE Condensed SRD](https://fate-srd.com/fate-condensed/get-started)** – The full system reference
- **[Official FATE Condensed PDF](https://www.evilhat.com/home/fate-condensed/)** – Free download from Evil Hat

## Quick Reference

Below are campaign-specific resources and rules clarifications, organized by topic.

{% assign groups = site.info | group_by: "topic" | sort_natural: "name" %}
{% for group in groups %}

  {% assign has_content = false %}
  {% for doc in group.items %}
  {% unless doc.tags contains "nested" %}
  {% assign has_content = true %}
  {% endunless %}
  {% endfor %}

  {% if has_content %}
  <h3>{{ group.name }}</h3>
  <ul>
  {% assign items = group.items | sort: "title" %}
  {% for doc in items %}
  {% unless doc.tags contains "nested" %}
    <li><a href="{{ doc.url | relative_url }}">{{ doc.title }}</a>{% if doc.summary %} — {{ doc.summary }}{% endif %}</li>
  {% endunless %}
  {% endfor %}
  </ul>
  {% endif %}
{% endfor %}

---

*New to FATE? Start with the [Get Started](https://fate-srd.com/fate-condensed/get-started) section of the SRD.*
