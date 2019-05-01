---
title: Project directory
subtitle: Other activities
layout: page
show_sidebar: false
tabs: example_tabs
---

<div class="columns is-multiline">
    {% for post in site.posts %}
      {% if post.category == 'other' %}
        <div class="column is-12">
            {% include entry.html %}
        </div>
      {% endif %}
    {% endfor %}
</div>
