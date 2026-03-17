---
permalink: /outdoors/
title: "Outdoors"
author_profile: true
---

# Catch Reports

{% for post in site.categories.outdoors %}
- [{{ post.title }}]({{ post.url }}) — {{ post.date | date: "%B %d, %Y" }}
{% endfor %}

## Debug Info
{% for post in site.categories.outdoors %}
- Title: {{ post.title }}
- URL: {{ post.url }}
- Path: {{ post.path }}
- Permalink: {{ post.permalink | default: "not set" }}
{% endfor %}
This will show you the actual URLs being generated. Common issues:

Common URL Problems:
1. Missing file extension in filename
Your post file should be named like: 2026-03-15-falls-lake.md (with .md extension)

2. Wrong folder location
Posts must be in the _posts folder at your site root:

text
your-site/
├── _posts/
│   └── 2026-03-15-falls-lake.md
├── outdoors.md
└── ...
3. Permalink structure in _config.yml
Check your _config.yml for permalink settings. Common formats:

yaml
permalink: /:year/:month/:day/:title/  # Results in /2026/03/15/falls-lake/
# or
permalink: /:categories/:title/        # Results in /outdoors/falls-lake/
# or
permalink: pretty                       # Default Jekyll format
4. Future dating issue
Your post is dated 2026-06-12. If you're testing locally, Jekyll might not show future posts. Either:

Change the date to today or earlier

Or run Jekyll with: jekyll serve --future

Quick Fix: Add permalink to your post
Force a specific URL by adding a permalink to your post front matter:

yaml
---
title: "Falls Lake Catch Report"
date: 2026-03-15
categories: outdoors
tags: [fishing, bass]
permalink: /outdoors/falls-lake/
---

## Falls Lake – June 12
...
Then update your link to use that permalink structure.

Check the actual URL
After running the debug code above, you'll see the actual URLs. They should look something like:

/2026/03/15/falls-lake.html

/outdoors/falls-lake/

/falls-lake.html

Whatever URL shows up in the debug output is what you need to use. If it shows something like /2026-03-15-falls-lake.html without a proper path, you may need to configure your permalinks in _config.yml.

Can you run the debug code and share what URLs are being generated? That will tell us exactly what's wrong.



