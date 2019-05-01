---
title: Project directory
subtitle: Data-driven projects
layout: page
show_sidebar: false
tabs: example_tabs
---

<div class="columns is-multiline">
    {% for post in site.posts %}
      {% if post.category == 'data' %}
        <div class="column is-12">
            {% include entry.html %}
        </div>
      {% endif %}
    {% endfor %}
</div>
