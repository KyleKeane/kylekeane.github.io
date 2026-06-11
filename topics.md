---
layout: default
title: Browse by topic
permalink: /topics.html
description: The full record sliced by topic — places, institutions, subjects, and formats, each with its own filtered view.
---

## Overview

Every entry in [the full record](/cv.html) carries topic tags —
places, institutions, subjects, and formats — alongside its persona
and principle tags. Each topic below links to a filtered view showing
every tagged entry. The list is generated from the tags themselves, so
new topics appear here automatically.

## All topics

{% assign all_tags = "" | split: "" %}
{%- for item in site.cv -%}
  {%- if item.specialties -%}
    {%- assign all_tags = all_tags | concat: item.specialties -%}
  {%- endif -%}
{%- endfor -%}
{%- assign all_tags = all_tags | uniq | sort %}
<ul>
{%- for tag in all_tags %}
{%- assign matches = site.cv | where_exp: "item", "item.specialties contains tag" %}
{%- assign tp = site.pages | where: "specialty_page", tag | first %}
{%- if tp %}
<li><a href="{{ tp.url | relative_url }}">{{ tp.title | remove_first: "Topic: " }}</a> ({{ matches.size }} entries)</li>
{%- else %}
<li>{{ tag }} ({{ matches.size }} entries)</li>
{%- endif %}
{%- endfor %}
</ul>
