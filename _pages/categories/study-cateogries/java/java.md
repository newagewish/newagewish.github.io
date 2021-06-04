---
title: "Java"
layout: custom/study-archive
permalink: categories/java
author_profile: true
sidebar:
 nav: temp
---

{% assign posts = site.categories.Java %}
{% for post in posts %} {% include custom/study-archive-single.html type=page.entries_layout %} {% endfor %}