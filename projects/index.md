---
layout: page
tagline:
title: Projects
---

# Personal Projects
{% assign project_dir = page.path | split:"/" | first %}
{% for p in site.pages %}
    {% if p.path != page.path %}
        {% assign top_dir = p.path | split:"/" | first %}
        {% if top_dir == project_dir %}
- [{{ p.title }}]({{ p.url }})
        {% endif %}
    {% endif %}
{% endfor %}

# Contributions and Forks
{% for repository in site.github.public_repositories %}
    {% if repository.fork == true %}
- [{{ repository.name }}]({{ repository.homepage }}): {{ repository.description }} {{ repository.parent.full_name }}
    {% endif %}
{% endfor %}
