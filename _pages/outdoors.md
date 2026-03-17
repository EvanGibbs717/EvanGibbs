---
permalink: /outdoors/
title: "Outdoors"
author_profile: true
---

# Fishing Reports

{% for post in site.categories.outdoors %}
- [{{ post.title }}]({{ site.baseurl }}{{ post.url }}) — {{ post.date | date: "%B %d, %Y" }}
{% endfor %}

