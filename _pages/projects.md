---
layout: archive
title: "Projects"
permalink: /project/
author_profile: true
---

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

  .project-card:hover {
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
    transform: translateY(-2px);
  }

  html[data-theme="dark"] .project-card {
    background: rgba(67, 68, 72, 0.65);
    border: 1px solid rgba(148, 163, 184, 0.35);
    box-shadow: 0 10px 24px rgba(2, 6, 23, 0.65);
  }

  html[data-theme="dark"] .project-card:hover {
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.4);
  }

  .project-card-content {
    padding: 1.5rem;
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
    line-height: 1.4;
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

  .project-image {
    width: 100%;
    height: 220px;
    object-fit: cover;
    border-radius: 12px;
    margin-top: 1.25rem;
    box-shadow: 0 10px 30px rgba(15,23,42,0.15);
    transition: transform 0.3s ease;
  }

  .project-card:hover .project-image {
    transform: scale(1.02);
  }

  .project-why {
    font-size: 0.9rem;
    color: var(--global-text-color);
    font-weight: 400;
    font-style: normal;
    margin: 0.5rem 0 1rem 0;
    line-height: 1.5;
    opacity: 0.85;
  }

  .project-why i {
    color: var(--global-link-color);
    margin-right: 6px;
    font-size: 0.85rem;
  }

  .tech-stack {
    display: flex;
    flex-wrap: wrap;
    gap: 0.4rem;
    margin-top: 1.25rem;
    padding-top: 1rem;
    border-top: 1px solid var(--global-border-color);
  }

  .tech-badge {
    display: inline-block;
    padding: 0.3rem 0.7rem;
    background: transparent;
    color: var(--global-text-color-light);
    border-radius: 4px;
    font-size: 0.75rem;
    font-weight: 500;
    border: 1px solid var(--global-border-color);
    transition: all 0.2s ease;
  }

  .tech-badge:hover {
    border-color: var(--global-link-color);
    color: var(--global-link-color);
  }

  html[data-theme="dark"] .tech-badge {
    border-color: rgba(148, 163, 184, 0.3);
  }

  .project-links {
    display: flex;
    gap: 0.6rem;
    margin-top: 1.25rem;
    flex-wrap: wrap;
  }

  .project-btn {
    display: inline-flex;
    align-items: center;
    gap: 0.4rem;
    padding: 0.5rem 1rem;
    background: transparent;
    color: var(--global-text-color);
    border-radius: 6px;
    text-decoration: none;
    font-size: 0.85rem;
    font-weight: 500;
    transition: all 0.2s ease;
    border: 1px solid var(--global-border-color);
  }

  .project-btn:hover {
    border-color: var(--global-link-color);
    color: var(--global-link-color);
    background: transparent;
  }

  .project-btn i {
    font-size: 0.8rem;
  }

  /* Featured Projects - Enhanced UI */
  .featured-card {
    background-color: #f9f9f9;
    border: 1px solid var(--global-border-color);
    border-radius: 18px;
    padding: 1.75rem;
    box-shadow: 0 20px 40px rgba(15, 23, 42, 0.08);
    transition: all 0.3s ease;
    display: flex;
    flex-direction: column;
  }

  .featured-card:hover {
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
    transform: translateY(-2px);
  }

  html[data-theme="dark"] .featured-card {
    background: rgba(67, 68, 72, 0.65);
    border: 1px solid rgba(148, 163, 184, 0.35);
    box-shadow: 0 10px 24px rgba(2, 6, 23, 0.65);
  }

  .featured-image {
    width: 100%;
    height: 220px;
    object-fit: cover;
    border-radius: 12px;
    margin-top: 1.25rem;
    box-shadow: 0 10px 30px rgba(15,23,42,0.15);
    transition: transform 0.3s ease;
  }

  .featured-card:hover .featured-image {
    transform: scale(1.02);
  }

  .featured-content {
    display: flex;
    flex-direction: column;
    flex: 1;
  }

  .featured-header {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    margin-bottom: 1rem;
    gap: 0.5rem;
  }

  .featured-title {
    font-size: 1.2rem;
    font-weight: 700;
    color: var(--global-text-color);
    margin: 0;
    line-height: 1.4;
  }

  .featured-date {
    font-size: 0.85rem;
    color: var(--global-text-color-light);
    font-weight: 600;
  }

  .featured-subtitle {
    font-size: 0.95rem;
    font-weight: 600;
    color: var(--global-link-color);
    margin: 0 0 0.75rem 0;
  }

  .featured-why {
    display: flex;
    align-items: flex-start;
    gap: 0.5rem;
    padding: 1rem;
    background: rgba(59, 130, 246, 0.05);
    border-left: 3px solid var(--global-link-color);
    border-radius: 0 6px 6px 0;
    margin: 1rem 0;
    font-size: 0.9rem;
    line-height: 1.6;
    color: var(--global-text-color);
  }

  .featured-why i {
    color: var(--global-link-color);
    font-size: 1rem;
    margin-top: 2px;
    flex-shrink: 0;
  }

  html[data-theme="dark"] .featured-why {
    background: rgba(59, 130, 246, 0.08);
  }

  .featured-description {
    font-size: 0.95rem;
    line-height: 1.7;
    color: var(--global-text-color);
    margin-bottom: 1.25rem;
    flex: 1;
  }

  .featured-tech-stack {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
    margin-bottom: 1.25rem;
    padding-bottom: 1.25rem;
    border-bottom: 1px solid var(--global-border-color);
  }

  .featured-tech-badge {
    padding: 0.4rem 0.85rem;
    background: var(--global-code-background-color);
    color: var(--global-text-color);
    border-radius: 6px;
    font-size: 0.8rem;
    font-weight: 600;
    border: 1px solid #d1d5db;
    transition: all 0.2s ease;
  }

  .featured-tech-badge:hover {
    border-color: var(--global-link-color);
    background: rgba(59, 130, 246, 0.1);
    color: var(--global-link-color);
  }

  html[data-theme="dark"] .featured-tech-badge {
    background: rgba(59, 130, 246, 0.1);
    color: #93c5fd;
    border-color: rgba(148, 163, 184, 0.3);
  }

  html[data-theme="dark"] .featured-tech-badge:hover {
    background: rgba(59, 130, 246, 0.2);
    border-color: #60a5fa;
  }

  .featured-links {
    display: flex;
    gap: 0.75rem;
  }

  .featured-btn {
    flex: 1;
    display: inline-flex;
    align-items: center;
    justify-content: center;
    gap: 0.5rem;
    padding: 0.65rem 1.25rem;
    border-radius: 8px;
    text-decoration: none;
    font-size: 0.9rem;
    font-weight: 600;
    transition: all 0.2s ease;
    border: 2px solid var(--global-link-color);
  }

  .featured-btn.primary {
    background: var(--global-link-color);
    color: #ffffff;
  }

  .featured-btn.primary:hover {
    background: var(--global-link-color);
    filter: brightness(0.85);
    border-color: transparent;
    color: #ffffff !important;
    transform: translateY(-1px);
    box-shadow: 0 4px 12px rgba(59, 130, 246, 0.3);
    text-decoration: none;
  }

  .featured-btn.secondary {
    background: transparent;
    color: var(--global-link-color);
  }

  .featured-btn.secondary:hover {
    background: rgba(59, 130, 246, 0.1);
    transform: translateY(-1px);
  }

  .featured-btn i {
    font-size: 0.85rem;
  }

  /* SECTION TITLE STYLES */
  h2.section-title {
    font-size: 1.4rem;
    font-weight: 700;
    color: var(--global-text-color);
    border-bottom: 2px solid var(--global-border-color);
    padding-bottom: 0.5rem;
    margin-top: 3rem;
    margin-bottom: 1.5rem;
    text-transform: uppercase;
    letter-spacing: 0.5px;
  }

  h2.section-title:first-of-type {
    margin-top: 1.5rem;
  }

  h2.section-title i {
    color: var(--global-link-color);
    margin-right: 10px;
    font-size: 1.2rem;
  }

  /* Visual Projects - Row Layout */
  .visual-projects-list {
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
    margin-top: 1.5rem;
  }

  .visual-project-card {
    background-color: #f9f9f9;
    border: 1px solid var(--global-border-color);
    border-radius: 18px;
    padding: 2rem;
    box-shadow: 0 20px 40px rgba(15, 23, 42, 0.08);
    display: flex;
    flex-direction: row;
    gap: 2.5rem;
    align-items: center;
    transition: all 0.3s ease;
  }

  .visual-project-card:hover {
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
    transform: translateY(-2px);
  }

  html[data-theme="dark"] .visual-project-card {
    background: rgba(67, 68, 72, 0.65);
    border: 1px solid rgba(148, 163, 184, 0.35);
    box-shadow: 0 10px 24px rgba(2, 6, 23, 0.65);
  }

  .visual-project-content {
    flex: 1;
    padding-right: 2rem;
  }

  .visual-project-image-container {
    flex: 1.2;
    max-width: 60%;
    display: flex;
    justify-content: flex-end;
  }

  .visual-project-image {
    width: 100%;
    height: auto;
    border-radius: 12px;
    box-shadow: 0 10px 30px rgba(15,23,42,0.15);
    object-fit: cover;
    aspect-ratio: 16/9;
  }

  @media (max-width: 768px) {
    .visual-project-card {
      flex-direction: column;
    }
    .visual-project-image-container {
      max-width: 100%;
    }
  }
</style>

{% include base_path %}

<p>
  Here you will find updates on my ongoing engineering tasks, simulation demos, and projects milestone.
</p>



<h2 class="section-title"><i class="fas fa-star"></i> Featured Projects</h2>

<div class="projects-grid">
{% for project in site.data.projects.featured_projects %}
  <div class="featured-card">
    <div class="featured-content">
      <div class="featured-header">
        <h2 class="featured-title">{{ project.title }}</h2>
        <span class="featured-date">{{ project.date }}</span>
      </div>

      <div class="featured-subtitle">{{ project.subtitle }}</div>

      {% if project.image %}
      <img src="{{ project.image }}" alt="{{ project.title }}" class="featured-image">
      {% endif %}

      {% if project.why %}
      <div class="featured-why">
        <i class="fas fa-lightbulb"></i>
        <span>{{ project.why }}</span>
      </div>
      {% endif %}

      <div class="featured-description">
        {{ project.description }}
      </div>

      {% if project.tech_stack %}
      <div class="featured-tech-stack">
        {% for tech in project.tech_stack %}
        <span class="featured-tech-badge">{{ tech }}</span>
        {% endfor %}
      </div>
      {% endif %}

      {% if project.github_url or project.demo_url %}
      <div class="featured-links">
        {% if project.github_url != "" %}
        <a href="{{ project.github_url }}" target="_blank" class="featured-btn primary">
          <i class="fab fa-github"></i> View Code
        </a>
        {% endif %}
        {% if project.demo_url != "" %}
        <a href="{{ project.demo_url }}" target="_blank" class="featured-btn secondary">
          <i class="fas fa-external-link-alt"></i> Live Demo
        </a>
        {% endif %}
      </div>
      {% endif %}
    </div>
  </div>
{% endfor %}
</div>



<h2 class="section-title"><i class="fas fa-chart-pie"></i> Visual Showcase</h2>

<div class="visual-projects-list">
{% for project in site.data.projects.visual_projects %}
  <div class="visual-project-card">
    <div class="visual-project-content">
      <div class="project-header">
        <h2 class="project-title">{{ project.title }}</h2>
        <span class="project-date">{{ project.date }}</span>
      </div>

      <div class="project-subtitle">{{ project.subtitle }}</div>

      <div class="project-description">
        {{ project.description }}
      </div>
    </div>

    {% if project.image %}
    <div class="visual-project-image-container">
      <img src="{{ project.image }}" alt="{{ project.title }}" class="visual-project-image">
    </div>
    {% endif %}
  </div>
{% endfor %}
</div>