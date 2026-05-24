---
title: Portfolio & Projects
layout: page
permalink: /portfolio/
---

# 🚀 My Portfolio

A collection of projects that showcase my skills, learning experiences, and passion for building great software.

<div class="portfolio-grid">
  {% for project in site.projects %}
    <div class="portfolio-item">
      <h3><a href="{{ project.url }}">{{ project.title }}</a></h3>
      <p>{{ project.description }}</p>
      <div class="tech-badges">
        {% for tech in project.tech_stack %}
          <span class="badge">{{ tech }}</span>
        {% endfor %}
      </div>
      <a href="{{ project.url }}" class="read-more">View Project →</a>
    </div>
  {% endfor %}
</div>

<style>
  .portfolio-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
    gap: 2em;
    margin-top: 2em;
  }

  .portfolio-item {
    background-color: rgba(15, 20, 25, 0.5);
    border: 1px solid #626A73;
    border-radius: 8px;
    padding: 1.5em;
    transition: all 0.3s ease;
  }

  .portfolio-item:hover {
    border-color: #FF8F40;
    box-shadow: 0 4px 12px rgba(255, 143, 64, 0.2);
    transform: translateY(-4px);
  }

  .portfolio-item h3 {
    margin: 0 0 0.75em 0;
  }

  .portfolio-item h3 a {
    color: #FFB454;
  }

  .portfolio-item p {
    color: #E6E1CF;
    font-size: 0.95em;
    margin: 0.5em 0 1em 0;
  }

  .tech-badges {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5em;
    margin: 1em 0;
  }
</style>
