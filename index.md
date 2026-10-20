---
layout: default
title: Dashboard
nav_order: 1
permalink: /
description: "Official academic learning hub, module notes, lecture timetables, and resource directory for Year Two Computer Science students at the University of Makeni."
---

<div class="hub-hero">
  <div class="hub-hero-badge">University of Makeni &bull; Faculty of Information Technology</div>
  <h1>Year Two Computer Science Learning Hub</h1>
  <p>
    Welcome to the central academic portal for Year Two Computer Science students. Access official course module notes, weekly lecture timetables, practical laboratory guidelines, and archived freshman materials.
  </p>
  <div class="hub-hero-meta">
    <span>🏛️ University of Makeni</span>
    <span>🎓 Class of 2027 (Year 2)</span>
    <span>📅 2025/2026 Academic Session</span>
    <span>📍 Main Campus, Makeni</span>
  </div>
</div>

## Quick Navigation
{: .text-delta .text-muted }

<div class="hub-quickgrid">
  <a href="{{ site.baseurl }}/modules/" class="hub-quickcard">
    <div class="hub-quickcard-icon">📚</div>
    <h3>Year Two Modules</h3>
    <p>Explore 10 semester modules, lecture slides, assignments, and reading materials.</p>
  </a>

  <a href="{{ site.baseurl }}/timetable/" class="hub-quickcard">
    <div class="hub-quickcard-icon">🗓️</div>
    <h3>Timetable & Notices</h3>
    <p>View the weekly class schedule, lab venue allocations, and departmental notices.</p>
  </a>

  <a href="{{ site.baseurl }}/archive/year-1/" class="hub-quickcard">
    <div class="hub-quickcard-icon">📂</div>
    <h3>Year One Archive</h3>
    <p>Reference past freshman lecture notes, tutorial sheets, and examination papers.</p>
  </a>

  <a href="{{ site.baseurl }}/resources/" class="hub-quickcard">
    <div class="hub-quickcard-icon">💻</div>
    <h3>Lab & Resources</h3>
    <p>Development tools setup (JDK, Git, VS Code), library guides, and ICT lab rules.</p>
  </a>
</div>

<div class="hub-section-header">
  <h2>Departmental Notice Board</h2>
  <a href="{{ site.baseurl }}/timetable/#announcements" class="hub-section-link">All Notices &rarr;</a>
</div>

<div class="hub-notice-feed">
  {% for notice in site.data.announcements limit: 3 %}
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

<div class="hub-section-header">
  <h2>Weekly Schedule Overview</h2>
  <a href="{{ site.baseurl }}/timetable/" class="hub-section-link">Full Timetable Details &rarr;</a>
</div>

<div class="hub-table-wrapper">
  <table class="hub-schedule-table">
    <thead>
      <tr>
        <th style="width: 14%;">Day</th>
        <th style="width: 22%;">Time</th>
        <th style="width: 38%;">Module & Lecturer</th>
        <th style="width: 26%;">Venue & Mode</th>
      </tr>
    </thead>
    <tbody>
      {% for d in site.data.timetable.days %}
        {% for s in d.sessions %}
        <tr>
          <td><span class="session-day-badge">{{ d.name }}</span></td>
          <td><strong>{{ s.time }}</strong></td>
          <td>
            <span class="session-code">{{ s.module_code }}</span>: <span class="session-module">{{ s.module_name }}</span>
            <small style="color: #64748b; font-size: 0.8rem;">{{ s.lecturer }}</small>
          </td>
          <td>
            <span class="session-venue">{{ s.venue }}</span>
            <span class="session-pill type-{{ s.type | slugify }}">{{ s.type }}</span>
          </td>
        </tr>
        {% endfor %}
      {% endfor %}
    </tbody>
  </table>
</div>

{% include leadership-section.html %}

