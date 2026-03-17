---
permalink: /outdoors/
title: "Outdoors"
author_profile: true

# Catch Reports

{% for post in site.categories.outdoors %}
- [{{ post.title }}]({{ post.url }}) — {{ post.date | date: "%B %d, %Y" }}
{% endfor %}
