---
title: "GitHub Pages Tips"
tags: Tech
---

I've been working with [GitHub Pages](https://pages.github.com/) lately. For a simple integration of [Project Pages](https://help.github.com/articles/user-organization-and-project-pages/#project-pages) into [User Pages](https://help.github.com/articles/user-organization-and-project-pages/#user--organization-pages) the following code snippet comes in handy

```
---
title: your-project-name-an-github
---

{% raw %}
{% for r in site.github.public_repositories %}
    {% if r.name == page.title %}
        {% assign repository = r %}
    {% endif %}
{% endfor %}
{% endraw %}
```

If `title` matches your repository name the variable repository will contain repository information like name, description and URLs.

E.g. my [vagrant-jekyll-gh-pages](https://github.com/vsaw/vagrant-jekyll-gh-pages) repository has the following [metadata](https://api.github.com/repos/vsaw/vagrant-jekyll-gh-pages)
