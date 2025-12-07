---
layout: archive
title: "Curriculum Vitae"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

<p style="margin-bottom: 2rem;">
  Here is a comprehensive overview of my professional experience, education, and technical skills. You can also view or download my resume.
</p>

<style>
  /* PROFESSIONAL CV STYLES */
  
  /* 1. General Typography */
  h2.cv-section-title {
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

  h2.cv-section-title i {
    color: var(--global-link-color);
    margin-right: 10px;
    font-size: 1.2rem;
  }

  /* 2. Timeline Layout (Date Left, Content Right) */
  .cv-entry {
    display: flex;
    margin-bottom: 1.5rem;
    gap: 20px;
  }

  .cv-date {
    flex: 0 0 130px; /* Fixed width for dates */
    font-weight: 600;
    color: var(--global-text-color-light);
    font-size: 0.95rem;
    text-align: right;
    padding-top: 2px;
  }

  .cv-content {
    flex: 1;
  }

  .cv-job-title {
    font-size: 1.1rem;
    font-weight: 700;
    color: var(--global-text-color);
    margin-bottom: 0.2rem;
  }

  .cv-company {
    font-size: 0.95rem;
    font-weight: 500;
    color: var(--global-text-color-light);
    font-style: italic;
    margin-bottom: 0.5rem;
    display: block;
  }

  .cv-location {
    font-size: 0.85rem;
    color: var(--global-text-color-light);
    margin-left: 5px;
    font-style: normal;
    opacity: 0.85;
  }

  .cv-content ul {
    margin: 0.5rem 0 0 1rem;
    padding: 0;
    font-size: 0.95rem;
    color: var(--global-text-color);
    line-height: 1.6;
  }

  /* 3. Skill Tags */
  .skills-container {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    margin-bottom: 1rem;
  }

  .skill-category {
    font-weight: 600;
    color: var(--global-text-color);
    margin-bottom: 0.5rem;
    display: block;
  }

  .skill-tag {
    background-color: color-mix(in srgb, var(--global-border-color) 50%, var(--global-bg-color));
    border: 1px solid var(--global-border-color);
    color: var(--global-text-color);
    padding: 4px 10px;
    border-radius: 6px;
    font-size: 0.85rem;
    font-weight: 500;
  }

  html:not([data-theme="dark"]) .skill-tag {
    background-color: #f3f4f6;
    border-color: #d1d5db;
    color: #1f2933;
    box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.6);
  }

  /* 4. Button Styling */
  .btn-resume {
    display: inline-block;
    background-color: var(--global-text-color);
    color: var(--global-bg-color) !important;
    padding: 10px 20px;
    border-radius: 5px;
    text-decoration: none;
    font-weight: 600;
    transition: background-color 0.3s, color 0.3s;
    margin-bottom: 1rem;
  }

  .btn-resume:hover {
    background-color:rgb(151, 152, 152);;
    color: var(--global-bg-color) !important;
    text-decoration: none;
  }

  /* Mobile Responsive */
  @media (max-width: 768px) {
    .cv-entry {
      flex-direction: column;
      gap: 5px;
    }
    .cv-date {
      text-align: left;
      flex: none;
      color: var(--global-link-color);
      font-size: 0.9rem;
    }
  }
</style>

<!-- DOWNLOAD BUTTON -->
<div style="text-align: left;">
  <a href="{{ site.baseurl }}/files/Resume_BitanMallik.pdf" target="_blank" class="btn-resume">
    <i class="fas fa-file-download"></i> View Resume
  </a>
</div>

<!-- WORK EXPERIENCE -->
<h2 class="cv-section-title"><i class="fas fa-briefcase"></i> Work Experience</h2>

{% for job in site.data.cv.work_experience %}
<div class="cv-entry">
  <div class="cv-date">{{ job.date }}</div>
  <div class="cv-content">
    <div class="cv-job-title">{{ job.title }}</div>
    <span class="cv-company">{{ job.company }} <span class="cv-location">• {{ job.location }}</span></span>
    <ul>
      {% for point in job.points %}
      <li>{{ point }}</li>
      {% endfor %}
    </ul>
  </div>
</div>
{% endfor %}


<!-- EDUCATION -->
<h2 class="cv-section-title"><i class="fas fa-graduation-cap"></i> Education</h2>

{% for edu in site.data.cv.education %}
<div class="cv-entry">
  <div class="cv-date">{{ edu.date }}</div>
  <div class="cv-content">
    <div class="cv-job-title">{{ edu.title }}</div>
    <span class="cv-company">{{ edu.company }} <span class="cv-location">• {{ edu.location }}</span></span>
    {% if edu.points.size > 0 %}
    <ul>
      {% for point in edu.points %}
      <li>{{ point }}</li>
      {% endfor %}
    </ul>
    {% endif %}
  </div>
</div>
{% endfor %}


<!-- TECHNICAL SKILLS -->
<h2 class="cv-section-title"><i class="fas fa-tools"></i> Technical Skills</h2>

{% for skill in site.data.cv.skills %}
<div class="cv-entry">
  <div class="cv-date">{{ skill.category }}</div>
  <div class="cv-content skills-container">
    {% for tag in skill.tags %}
    <span class="skill-tag">{{ tag }}</span>
    {% endfor %}
  </div>
</div>
{% endfor %}


<!-- ACADEMIC PROJECTS -->
<h2 class="cv-section-title"><i class="fas fa-project-diagram"></i> Academic Projects</h2>

{% for project in site.data.cv.academic_projects %}
<div class="cv-entry">
  <div class="cv-date">{{ project.date }}</div>
  <div class="cv-content">
    <div class="cv-job-title">{{ project.title }}</div>
    <span class="cv-company">{{ project.company }}</span>
    <ul>
      {% for point in project.points %}
      <li>{{ point }}</li>
      {% endfor %}
    </ul>
  </div>
</div>
{% endfor %}


<!-- CERTIFICATIONS & AWARDS GRID -->
<div style="display: flex; flex-wrap: wrap; gap: 2rem; margin-top: 2rem;">
  
  <!-- Certifications -->
  <div style="flex: 1; min-width: 300px;">
    <h2 class="cv-section-title" style="margin-top: 0;"><i class="fas fa-certificate"></i> Certifications</h2>
    <ul style="color: var(--global-text-color); line-height: 1.6;">
      {% for cert in site.data.cv.certifications_summary %}
      <li>{{ cert }}</li>
      {% endfor %}
    </ul>
  </div>

  <!-- Awards -->
  <div style="flex: 1; min-width: 300px;">
    <h2 class="cv-section-title" style="margin-top: 0;"><i class="fas fa-trophy"></i> Awards</h2>
    <ul style="color: var(--global-text-color); line-height: 1.6;">
      {% for award in site.data.cv.awards_summary %}
      <li>{{ award }}</li>
      {% endfor %}
    </ul>
  </div>

</div>


<!-- LANGUAGES -->
<h2 class="cv-section-title"><i class="fas fa-language"></i> Languages</h2>
<div class="skills-container">
  {% for lang in site.data.cv.languages %}
  <span class="skill-tag">{{ lang }}</span>
  {% endfor %}
</div>