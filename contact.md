---
layout: page
title: Contact
order: 5
---

{% if site.email %}
- {% include icon-email.html %} by email
{% endif %}

{% if site.github_username %}
- {% include icon-github.html username=site.github_username %} on github
{% endif %}

{% if site.twitter_username %}
- {% include icon-twitter.html username=site.twitter_username %} on twitter
{% endif %}
