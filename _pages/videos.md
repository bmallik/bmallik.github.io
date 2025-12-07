---
layout: archive
title: "Videos"
permalink: /videos/
author_profile: true
---

{% include base_path %}

<style>
  .video-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 2rem;
    margin-top: 2rem;
  }

  .video-card {
    background: #fff;
    border: 1px solid #e2e8f0;
    border-radius: 12px;
    overflow: hidden;
    box-shadow: 0 4px 6px rgba(0,0,0,0.05);
    transition: transform 0.2s ease, box-shadow 0.2s ease;
  }

  .video-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 15px rgba(0,0,0,0.1);
  }

  html[data-theme="dark"] .video-card {
    background: #2d3748;
    border-color: #4a5568;
  }

  .video-wrapper {
    position: relative;
    padding-bottom: 56.25%; /* 16:9 aspect ratio */
    height: 0;
    overflow: hidden;
    background: #000;
  }

  .video-wrapper iframe,
  .video-wrapper video {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    border: 0;
    object-fit: cover;
  }

  .video-info {
    padding: 1.25rem;
  }

  .video-title {
    font-size: 1.1rem;
    font-weight: 700;
    margin-bottom: 0.5rem;
    color: var(--global-text-color);
  }

  .video-desc {
    font-size: 0.9rem;
    color: var(--global-text-color-light);
    line-height: 1.5;
  }
</style>

<p>
  A collection of videos demonstrating my projects, simulations, and talks.
</p>

<div class="video-grid">
  <!-- YouTube Video Example -->
  <div class="video-card">
    <div class="video-wrapper">
      <iframe 
        src="https://www.youtube.com/embed/14aikUdVScI" 
        title="High-Speed SerDes Transmitter"
        frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
        referrerpolicy="strict-origin-when-cross-origin"
        allowfullscreen>
      </iframe>
    </div>
    <div class="video-info">
      <div class="video-title">High-Speed SerDes Transmitter</div>
      <div class="video-desc">Demonstration of adaptive equalizer convergence and eye diagram simulation.</div>
    </div>
  </div>

  <!-- Local Video Example -->
  <div class="video-card">
    <div class="video-wrapper">
      <video muted loop playsinline webkit-playsinline controls preload="auto">
        <source src="{{ site.baseurl }}/files/313145_tiny_web.mp4" type="video/mp4">
        Your browser does not support the video tag.
      </video>
    </div>
    <div class="video-info">
      <div class="video-title">Mixed-Signal Layout Automation</div>
      <div class="video-desc">Automated layout generation tool for differential pairs using SKILL scripting.</div>
    </div>
  </div>
</div>
