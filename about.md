---
layout: dark
title: About
example: This is an example value.
---
This page describes the amazing {{ site.title }} by {{ site.author.name }}.
{{ page.example }}
{% include big-cat.html %}

## List of animals
{% for animal in site.data.animals %}
- The {{ animal.name }} is a {{ animal.size }} animal.
{% endfor %}

## Large animals are better
{% for animal in site.data.animals %}
{% if animal.size == "large" %}- <strong style="color: {{animal.color }};">
{{ animal.name}}</strong>
{% else %}- <small>{{ aniimal.name }}</small>
{% endif %}
{% endfor %}
  
## List of small animals
{% assign small_animals = site.data.animals | where: "size", "small" %}
{% for animal in small_animals %}
- {{ animale.name | upcase }}
{% endfor %}

Some Markdown content describing your site.

## About About Pages

The About page is a common convention found on websites.
It is your opportunity to let us know all the details "about" your project:

- focus and topic area
- people involved
- code and projects used
