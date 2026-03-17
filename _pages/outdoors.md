---
permalink: /outdoors/
title: "Outdoors"
author_profile: true
---

# Catch Reports

{% for post in site.categories.outdoors %}
- [[{{ post.title }}]({{ site.baseurl }}{{ post.url }})) — {{ post.date | date: "%B %d, %Y" }}
{% endfor %}

## Debug Info
Total posts in site: {{ site.posts | size }}
Posts in outdoors category: {{ site.categories.outdoors | size }}

{% if site.categories.outdoors.size == 0 %}
**No posts found in outdoors category**
{% else %}
**Posts found:**
{% for post in site.categories.outdoors %}
- Title: {{ post.title }}
- URL: {{ post.url }}
- Full URL: {{ site.url }}{{ post.url }}
- Path: {{ post.path }}
{% endfor %}
{% endif %}

