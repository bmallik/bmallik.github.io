---
layout: archive
title: "Certifications"
permalink: /certifications/
author_profile: true
---

{% include base_path %}

<p style="margin-bottom: 2rem;">
  Here you will find a collection of my professional certifications, scholarships, and academic projects, demonstrating my continuous dedication to technical mastery and engineering excellence.
</p>

<style>
  /* SHARED CV STYLES */
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

  .cv-entry {
    display: flex;
    margin-bottom: 1.5rem;
    gap: 20px;
  }

  .cv-date {
    flex: 0 0 130px;
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
  
  .cv-link {
    font-size: 0.9rem;
    display: inline-block;
    margin-top: 0.25rem;
    color: var(--global-link-color);
    text-decoration: none;
    font-weight: 500;
  }
  
  .cv-link:hover {
    text-decoration: underline;
  }
  
  @media (max-width: 768px) {
    .cv-entry {
      flex-direction: column;
      gap: 5px;
    }
    .cv-date {
      text-align: left;
      flex: 0 0 auto;
      margin-bottom: 5px;
    }
  }
</style>

<h2 class="cv-section-title"><i class="fas fa-certificate"></i> Professional Certifications</h2>

{% for item in site.data.certifications.certifications %}
<div class="cv-entry">
  <div class="cv-date">{{ item.date }}</div>
  <div class="cv-content">
    <div class="cv-job-title">{{ item.title }}</div>
    <span class="cv-company">{{ item.company }}</span>
    {% if item.link and item.link != "" %}
    <a href="{{ site.baseurl }}{{ item.link }}" target="_blank" class="cv-link"><i class="{{ item.icon }}"></i> {{ item.link_text }}</a>
    {% endif %}
  </div>
</div>
{% endfor %}

<h2 class="cv-section-title"><i class="fas fa-award"></i> Scholarships</h2>

{% for item in site.data.certifications.scholarships %}
<div class="cv-entry">
  <div class="cv-date">{{ item.date }}</div>
  <div class="cv-content">
    <div class="cv-job-title">{{ item.title }}</div>
    <span class="cv-company">{{ item.company }}</span>
    {% if item.link and item.link != "" %}
    <a href="{{ site.baseurl }}{{ item.link }}" target="_blank" class="cv-link"><i class="{{ item.icon }}"></i> {{ item.link_text }}</a>
    {% endif %}
  </div>
</div>
{% endfor %}

<h2 class="cv-section-title"><i class="fas fa-project-diagram"></i> Academic Projects & Presentations</h2>

{% for item in site.data.certifications.projects %}
<div class="cv-entry">
  <div class="cv-date">{{ item.date }}</div>
  <div class="cv-content">
    <div class="cv-job-title">{{ item.title }}</div>
    <span class="cv-company">{{ item.company }}</span>
    {% if item.link and item.link != "" %}
    <a href="{{ site.baseurl }}{{ item.link }}" target="_blank" class="cv-link"><i class="{{ item.icon }}"></i> {{ item.link_text }}</a>
    {% endif %}
  </div>
</div>
{% endfor %}