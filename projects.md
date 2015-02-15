---
layout: page
tagline:
permalink: projects.html
title: Projects
---

# Personal Projects
{% for repository in site.github.public_repositories %}
    {{ if repository.fork == false }}
        {{ if repository.has_pages }}
- [{{ repository.name }}]({{ repository.homepage }}): {{ repository.description }}
        {% endif %}
    {% endif %}
{% endfor %}

# Contributions and Forks
{% for repository in site.github.public_repositories %}
    {{ if repository.fork }}
- [{{ repository.name }}]({{ repository.homepage }}): {{ repository.description }}
    {% endif %}
{% endfor %}
