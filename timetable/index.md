---
layout: default
title: Timetable & Notices
nav_order: 3
permalink: /timetable/
description: "Weekly lecture timetable, lab allocations, and official departmental notices for Year Two Computer Science at the University of Makeni."
---

# Timetable & Notices
{: .fs-9 }

University of Makeni &bull; First Semester 2025/2026
{: .fs-5 .text-delta .text-muted }

---

## Weekly Lecture & Practical Schedule
{: .text-delta }

> #### 📍 Venue & Lab Allocations
> - **Lectures:** Lecture Hall A, Lecture Hall B, and Hall 3 (Faculty of IT).
> - **Practical Labs:** Main ICT Lab, ICT Lab 1, and ICT Lab 2.
> - **Studio Sessions:** University Innovation Hub.
{: .note }

{% for d in site.data.timetable.days %}
### {{ d.name }}
{: .fs-6 }

<div class="hub-table-wrapper">
  <table class="hub-schedule-table">
    <thead>
      <tr>
        <th style="width: 22%;">Time</th>
        <th style="width: 15%;">Module</th>
        <th style="width: 33%;">Title & Lecturer</th>
        <th style="width: 15%;">Venue</th>
        <th style="width: 15%;">Type</th>
      </tr>
    </thead>
    <tbody>
      {% for s in d.sessions %}
      <tr>
        <td><strong>{{ s.time }}</strong></td>
        <td><span class="session-code">{{ s.module_code }}</span></td>
        <td>
          <span class="session-module">{{ s.module_name }}</span>
          <small style="color: #64748b;">{{ s.lecturer }}</small>
          {% if s.notes %}
          <div style="font-size: 0.775rem; color: #475569; margin-top: 2px;"><em>{{ s.notes }}</em></div>
          {% endif %}
        </td>
        <td><span class="session-venue">{{ s.venue }}</span></td>
        <td><span class="session-pill type-{{ s.type | slugify }}">{{ s.type }}</span></td>
      </tr>
      {% endfor %}
    </tbody>
  </table>
</div>
{% endfor %}

---

## Departmental Notice Board
{: #announcements .text-delta }

Official circulars, academic notices, and schedule updates issued by the Department of Computer Science:

<div class="hub-notice-feed">
  {% for notice in site.data.announcements %}
  <div class="hub-notice-card{% if notice.priority == 'high' %} priority-high{% endif %}">
    <div class="hub-notice-meta">
      <span class="hub-pill pill-{{ notice.category | downcase }}">{{ notice.category }}</span>
      <span class="hub-notice-date">{{ notice.date }}</span>
      {% if notice.author %}
      <span class="hub-notice-author">&middot; {{ notice.author }}</span>
      {% endif %}
    </div>
    <h4>{{ notice.title }}</h4>
    <p>{{ notice.content }}</p>
    {% if notice.action_link and notice.action_label %}
    <a href="{{ site.baseurl }}{{ notice.action_link }}" class="hub-notice-btn">{{ notice.action_label }} &rarr;</a>
    {% endif %}
  </div>
  {% endfor %}
</div>
