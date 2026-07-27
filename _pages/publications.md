---
title: "Publications"
permalink: /publications/
author_profile: true
---

# Journal Articles

{% assign manuscripts = site.publications | where: "category", "manuscripts" | sort: "date" | reverse %}
{% for post in manuscripts %}
  <div style="margin-bottom: 1em; padding-bottom: 1em; border-bottom: 1px solid #eee;">
    <a href="{{ post.url | relative_url }}"><strong>{{ post.title }}</strong></a><br/>
    <span style="color: #666; font-size: 0.9em;">{{ post.venue }} · {{ post.date | date: "%Y" }}</span>
    {% if post.paperurl %} · <a href="{{ post.paperurl }}">PDF</a>{% endif %}
    <details style="margin-top: 0.3em;">
      <summary style="cursor: pointer; font-size: 0.85em; color: #888;">Citation</summary>
      <p style="font-size: 0.85em; color: #666;">{{ post.citation }}</p>
    </details>
  </div>
{% endfor %}

# Conference Papers

{% assign conferences = site.publications | where: "category", "conferences" | sort: "date" | reverse %}
{% for post in conferences %}
  <div style="margin-bottom: 1em; padding-bottom: 1em; border-bottom: 1px solid #eee;">
    <a href="{{ post.url | relative_url }}"><strong>{{ post.title }}</strong></a><br/>
    <span style="color: #666; font-size: 0.9em;">{{ post.venue }} · {{ post.date | date: "%Y" }}</span>
    {% if post.paperurl %} · <a href="{{ post.paperurl }}">PDF</a>{% endif %}
    <details style="margin-top: 0.3em;">
      <summary style="cursor: pointer; font-size: 0.85em; color: #888;">Citation</summary>
      <p style="font-size: 0.85em; color: #666;">{{ post.citation }}</p>
    </details>
  </div>
{% endfor %}
