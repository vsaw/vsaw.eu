---
layout: page
tagline:
permalink: projects.html
title: Projects
---

# Personal Projects
{% for repository in site.github.public_repositories %}
    {% if repository.fork == false and repository.has_pages == true %}
        {% if repository.name != site.github.repository_name %}
- [{{ repository.name }}]({{ repository.homepage }}): {{ repository.description }}
        {% endif %}
    {% endif %}
{% endfor %}

# Contributions and Forks
{% for repository in site.github.public_repositories %}
    {% if repository.fork == true %}
- [{{ repository.name }}]({{ repository.homepage }}): {{ repository.description }} {{ repository.parent.full_name }}
    {% endif %}
{% endfor %}
