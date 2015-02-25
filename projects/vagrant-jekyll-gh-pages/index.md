---
title: vagrant-jekyll-gh-pages
description: Set up Jekyll to locally test GitHub Pages within minutes
---

{% for r in site.github.public_repositories %}
    {% if r.name == page.title %}
        {% assign repository = r %}
    {% endif %}
{% endfor %}


This will bootstrap a small ubuntu server running [Jekyll](http://jekyllrb.com/) configured by the [guidelines of GitHub Pages](https://help.github.com/articles/using-jekyll-with-pages/).

The **Requirements** are only [Vagrant](https://www.vagrantup.com/). The rest will be automatically retrieved and installed by the script.

# Getting Started
1. Clone the repository with `git clone {{ repository.clone_url }}`
2. Go inside the cloned project `cd {{ repository.name }}`
3. Start Vagrant `vagrant up`

That's it you're done and can immediately visit your page at [http://127.0.0.1:4000/](http://127.0.0.1:4000/)

# Advanced Administration
Jekyll is installed as a normal ubuntu service. You can control it directly using

```bash
# SSH into the vagrant container
$ vagrant ssh

# Control the service inside vagrant
$ sudo service jekyll (start|stop|restart|status)
```

# License
See [LICENSE]({{ repository.html_url }}/blob/{{ repository.default_branch }}/LICENSE)
