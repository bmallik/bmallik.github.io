---
layout: archive
title: "Activities"
permalink: /activity/
author_profile: true
---

{% include base_path %}

<style>
  .projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
    gap: 1.5rem;
    margin-top: 1.5rem;
  }

  .project-card {
    background-color: #f9f9f9;
    border: 1px solid var(--global-border-color);
    border-radius: 18px;
    padding: 1.75rem;
    box-shadow: 0 20px 40px rgba(15, 23, 42, 0.08);
    display: flex;
    flex-direction: column;
    min-height: 100%;
  }

  html[data-theme="dark"] .project-card {
    background: rgba(67, 68, 72, 0.65);
    border: 1px solid rgba(148, 163, 184, 0.35);
    box-shadow: 0 10px 24px rgba(2, 6, 23, 0.65);
  }

  .project-header {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    margin-bottom: 1rem;
    gap: 0.5rem;
  }

  .project-title {
    font-size: 1.3rem;
    font-weight: 700;
    margin: 0;
    color: var(--global-text-color);
  }

  .project-date {
    font-size: 0.9rem;
    color: var(--global-text-color-light);
    font-weight: 600;
  }

  .project-subtitle {
    font-size: 1rem;
    font-weight: 600;
    color: var(--global-link-color);
    margin: 0 0 0.75rem 0;
  }

  .project-description {
    font-size: 0.95rem;
    color: var(--global-text-color);
    line-height: 1.6;
    flex: 1;
  }

  .video-wrapper {
    position: relative;
    width: 100%;
    margin-top: 1.25rem;
    aspect-ratio: 16 / 9;
    overflow: hidden;
    border-radius: 12px;
    box-shadow: 0 10px 30px rgba(15,23,42,0.15);
    background: #000;
  }

  .video-wrapper iframe,
  .video-wrapper video {
    width: 100%;
    height: 100%;
    border: none;
    display: block;
  }

  /* SECTION TITLE STYLES */
  h2.activity-section-title {
    font-size: 1.4rem;
    font-weight: 700;
    color: var(--global-text-color);
    border-bottom: 2px solid var(--global-border-color);
    padding-bottom: 0.5rem;
    margin-top: 2.5rem;
    margin-bottom: 1.5rem;
    text-transform: uppercase;
    letter-spacing: 0.5px;
  }

  h2.activity-section-title i {
    color: var(--global-link-color);
    margin-right: 10px;
    font-size: 1.2rem;
  }

  /* TASK CARD STYLES */
  .task-card {
    background-color: #f9f9f9;
    border: 1px solid var(--global-border-color);
    border-radius: 18px;
    overflow: hidden;
    box-shadow: 0 20px 40px rgba(15, 23, 42, 0.08);
    display: flex;
    flex-direction: column;
  }

  html[data-theme="dark"] .task-card {
    background: rgba(67, 68, 72, 0.65);
    border: 1px solid rgba(148, 163, 184, 0.35);
    box-shadow: 0 10px 24px rgba(2, 6, 23, 0.65);
  }

  .task-image {
    width: 100%;
    height: 180px;
    object-fit: cover;
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  }

  .task-content {
    padding: 1.5rem;
    display: flex;
    flex-direction: column;
    flex: 1;
  }

  .task-header {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    margin-bottom: 0.5rem;
    gap: 0.5rem;
  }

  .task-title {
    font-size: 1.2rem;
    font-weight: 700;
    margin: 0;
    color: var(--global-text-color);
  }

  .task-date {
    font-size: 0.85rem;
    color: var(--global-text-color-light);
    font-weight: 600;
    white-space: nowrap;
  }

  .task-heading {
    font-size: 0.95rem;
    font-weight: 600;
    color: var(--global-link-color);
    margin: 0 0 0.75rem 0;
  }

  .task-description {
    font-size: 0.9rem;
    color: var(--global-text-color);
    line-height: 1.6;
    flex: 1;
  }

  /* CV-STYLE ENTRY CARDS */
  .cv-entry {
    display: flex;
    margin-bottom: 1.5rem;
    gap: 20px;
    padding: 1.25rem;
    background-color: #f9f9f9;
    border: 1px solid var(--global-border-color);
    border-radius: 12px;
    box-shadow: 0 4px 12px rgba(15, 23, 42, 0.05);
    transition: transform 0.2s ease, box-shadow 0.2s ease;
  }

  .cv-entry:hover {
    transform: translateY(-2px);
    box-shadow: 0 8px 20px rgba(15, 23, 42, 0.1);
  }

  html[data-theme="dark"] .cv-entry {
    background: rgba(67, 68, 72, 0.65);
    border: 1px solid rgba(148, 163, 184, 0.35);
    box-shadow: 0 4px 12px rgba(2, 6, 23, 0.4);
  }

  html[data-theme="dark"] .cv-entry:hover {
    box-shadow: 0 8px 20px rgba(2, 6, 23, 0.6);
  }

  .cv-icon {
    flex: 0 0 50px;
    display: flex;
    align-items: flex-start;
    justify-content: center;
    padding-top: 4px;
  }

  .cv-icon i {
    font-size: 1.5rem;
    color: var(--global-link-color);
  }

  .cv-content {
    flex: 1;
  }

  .cv-header {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    margin-bottom: 0.3rem;
    gap: 1rem;
  }

  .cv-title {
    font-size: 1.1rem;
    font-weight: 700;
    color: var(--global-text-color);
    margin: 0;
  }

  .cv-date {
    font-size: 0.85rem;
    font-weight: 600;
    color: var(--global-text-color-light);
    white-space: nowrap;
  }

  .cv-role {
    font-size: 0.95rem;
    font-weight: 600;
    color: var(--global-link-color);
    margin-bottom: 0.5rem;
  }

  .cv-venue {
    font-size: 0.9rem;
    font-weight: 500;
    color: var(--global-text-color-light);
    font-style: italic;
    margin-bottom: 0.5rem;
  }

  .cv-description {
    font-size: 0.9rem;
    color: var(--global-text-color);
    line-height: 1.6;
    margin: 0;
  }

  .cv-link {
    display: inline-block;
    margin-top: 0.5rem;
    font-size: 0.85rem;
    color: var(--global-link-color);
    text-decoration: none;
    font-weight: 500;
  }

  .cv-link:hover {
    text-decoration: underline;
  }

  .entries-list {
    display: flex;
    flex-direction: column;
    gap: 0;
  }

  @media (max-width: 768px) {
    .cv-entry {
      flex-direction: column;
      gap: 10px;
    }
    .cv-icon {
      flex: 0 0 auto;
      justify-content: flex-start;
    }
    .cv-header {
      flex-direction: column;
      gap: 0.25rem;
    }
  }
</style>

<p style="margin-bottom: 2rem;">
  Highlights of my professional engagement beyond research—demos, mentorship, events, and talks.
</p>

<h2 class="activity-section-title"><i class="fas fa-video"></i> Simulation Demos</h2>

<div class="projects-grid">
{% for item in site.data.activities.activities %}
  <div class="project-card">
    <div class="project-header">
      <h2 class="project-title">{{ item.title }}</h2>
      <span class="project-date">{{ item.date }}</span>
    </div>

    <div class="project-subtitle">{{ item.subtitle }}</div>

    <div class="project-description">
      {{ item.description }}
    </div>

    <div class="video-wrapper">
      {% if item.video_type == "youtube" %}
      <iframe 
        src="{{ item.video_url }}" 
        title="{{ item.title }}"
        frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
        referrerpolicy="strict-origin-when-cross-origin"
        allowfullscreen>
      </iframe>
      {% elsif item.video_type == "vimeo" %}
      <iframe src="{{ item.video_url }}?autoplay=1&muted=1&loop=1" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
      {% elsif item.video_type == "local" %}
      <video muted loop playsinline webkit-playsinline controls preload="auto">
        <source src="{{ site.baseurl }}{{ item.video_url }}" type="video/mp4">
        Your browser does not support the video tag.
      </video>
      {% endif %}
    </div>
  </div>
{% endfor %}
</div>

<h2 class="activity-section-title"><i class="fas fa-tasks"></i> Ongoing Tasks</h2>

<div class="projects-grid">
{% for task in site.data.activities.ongoing_tasks %}
  <div class="task-card">
    <img src="{{ task.image }}" alt="{{ task.title }}" class="task-image" onerror="this.style.display='none'">
    <div class="task-content">
      <div class="task-header">
        <h3 class="task-title">{{ task.title }}</h3>
        <span class="task-date">{{ task.date }}</span>
      </div>
      <div class="task-heading">{{ task.heading }}</div>
      <div class="task-description">{{ task.description }}</div>
    </div>
  </div>
{% endfor %}
</div>

<h2 class="activity-section-title"><i class="fas fa-calendar-alt"></i> Event Organization</h2>

<div class="entries-list">
{% for event in site.data.activities.event_organization %}
  <div class="cv-entry">
    <div class="cv-icon">
      <i class="{{ event.icon }}"></i>
    </div>
    <div class="cv-content">
      <div class="cv-header">
        <h3 class="cv-title">{{ event.title }}</h3>
        <span class="cv-date">{{ event.date }}</span>
      </div>
      <div class="cv-role">{{ event.role }}</div>
      <p class="cv-description">{{ event.description }}</p>
    </div>
  </div>
{% endfor %}
</div>

<h2 class="activity-section-title"><i class="fas fa-hands-helping"></i> Mentorship & Outreach</h2>

<div class="entries-list">
{% for item in site.data.activities.mentorship_outreach %}
  <div class="cv-entry">
    <div class="cv-icon">
      <i class="{{ item.icon }}"></i>
    </div>
    <div class="cv-content">
      <div class="cv-header">
        <h3 class="cv-title">{{ item.title }}</h3>
        <span class="cv-date">{{ item.date }}</span>
      </div>
      <div class="cv-role">{{ item.role }}</div>
      <p class="cv-description">{{ item.description }}</p>
    </div>
  </div>
{% endfor %}
</div>

<h2 class="activity-section-title"><i class="fas fa-microphone-alt"></i> Media & Invited Talks</h2>

<div class="entries-list">
{% for talk in site.data.activities.media_talks %}
  <div class="cv-entry">
    <div class="cv-icon">
      <i class="{{ talk.icon }}"></i>
    </div>
    <div class="cv-content">
      <div class="cv-header">
        <h3 class="cv-title">{{ talk.title }}</h3>
        <span class="cv-date">{{ talk.date }}</span>
      </div>
      <div class="cv-venue">{{ talk.venue }}</div>
      <p class="cv-description">{{ talk.description }}</p>
      {% if talk.link != "" %}
      <a href="{{ talk.link }}" target="_blank" class="cv-link"><i class="fas fa-external-link-alt"></i> {{ talk.link_text }}</a>
      {% endif %}
    </div>
  </div>
{% endfor %}
</div>