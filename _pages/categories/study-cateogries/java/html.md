---
title: "Html"
layout: custom/study-archive
permalink: categories/html
author_profile: true
sidebar:
 nav: temp
---

{% assign posts = site.categories.HTML %}
{% for post in posts %} {% include custom/study-archive-single.html type=page.entries_layout %} {% endfor %}