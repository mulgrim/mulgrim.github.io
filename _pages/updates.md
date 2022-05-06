---
layout: page
title: 'Updates'
description: 'improve little by little'
category: Updates
permalink: /updates/
---

<ul class="update-list">
    {% assign posts = site.posts | where: 'layout', 'update' | slice: 0, site.updates_count %}
      {%- for post in posts -%}
      <li><time datetime="{{ post.date }}">{{ post.date | date: "%b %d, %Y" }}</time><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
    {%- endfor -%}
</ul>