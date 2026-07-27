---
title: "Teaching & Outreach"
permalink: /teaching/
author_profile: true
---

# Academic teaching

{% assign academic = site.teaching | where: "type", "academic" %}
{% for post in academic %}
  <div style="margin-bottom: 2em;">
    <h3>{{ post.title }}</h3>
    <p>
      <strong>Level:</strong> {{ post.level }}<br/>
      <strong>Period:</strong> {{ post.period }}<br/>
      <strong>Location:</strong> {{ post.venue }}, {{ post.location }}
    </p>
    <p>{{ post.content }}</p>
  </div>
{% endfor %}

# Outreach

{% assign outreach = site.teaching | where: "type", "outreach" %}
{% for post in outreach %}
  <div style="margin-bottom: 1.5em;">
    <h4>{{ post.title }}</h4>
    <p>{{ post.content }}</p>
  </div>
{% endfor %}
