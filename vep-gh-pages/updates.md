---
layout: default
title: Updates
permalink: /updates
---

# Updates / Обновления

{% capture changelog %}{% include_relative CHANGELOG.md %}{% endcapture %}
{{ changelog | markdownify }}

## Dev Notes
- We'll also drop short posts to `_posts/` for big milestones.
