---
permalink: /outdoors/
title : Fishing Reports
author_profile: true
---

{% for post in site.categories.outdoors %}
- [{{ post.title }}]({{ site.baseurl }}{{ post.url }}) — {{ post.date | date: "%B %d, %Y" }}
{% endfor %}

