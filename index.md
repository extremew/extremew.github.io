---
title: Home
layout: default
permalink: /
---

<section class="hero">
  <div class="hero-content">
    <h1 class="hero-title">🚀 Welcome to My Tech Journey</h1>
    <p class="hero-subtitle">Exploring the intersection of code, creativity, and continuous learning</p>
    <div class="hero-cta">
      <a href="#featured-projects" class="btn">📂 Explore Projects</a>
      <a href="/learning/" class="btn secondary">📚 Read My Journey</a>
    </div>
  </div>
</section>

<section id="featured-projects" class="featured-projects">
  <h2>🌟 Featured Projects</h2>
  <div class="projects-grid">
    {% for project in site.projects limit:3 %}
      <div class="project-card">
        <h3><a href="{{ project.url }}">{{ project.title }}</a></h3>
        <p>{{ project.description }}</p>
        <div class="project-card-tech">
          {% for tech in project.tech_stack %}
            <span class="badge">{{ tech }}</span>
          {% endfor %}
        </div>
        <a href="{{ project.url }}" class="read-more">Read More →</a>
      </div>
    {% endfor %}
  </div>
  <div class="view-all">
    <a href="/portfolio/" class="btn">View All Projects →</a>
  </div>
</section>

<section class="latest-posts">
  <h2>📖 Latest from My Learning Journey</h2>
  <div class="posts-list">
    {% for post in site.posts limit:3 %}
      <article class="post-preview">
        <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
        <div class="post-meta">
          <span class="post-date">📅 {{ post.date | date: "%B %d, %Y" }}</span>
          {% if post.categories %}
            <div class="post-categories">
              {% for category in post.categories %}
                <span class="badge">{{ category }}</span>
              {% endfor %}
            </div>
          {% endif %}
        </div>
        <p>{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
        <a href="{{ post.url }}" class="read-more">Read More →</a>
      </article>
    {% endfor %}
  </div>
  <div class="view-all">
    <a href="/learning/" class="btn">View All Posts →</a>
  </div>
</section>

<style>
  .hero {
    text-align: center;
    padding: 4em 1em;
    background: linear-gradient(135deg, rgba(255, 143, 64, 0.1) 0%, rgba(170, 217, 76, 0.1) 100%);
    border-radius: 8px;
    margin-bottom: 3em;
    border: 1px solid #626A73;
  }

  .hero-title {
    font-size: 3em;
    margin: 0 0 0.5em 0;
    color: #FFB454;
  }

  .hero-subtitle {
    font-size: 1.3em;
    color: #AAD94C;
    margin: 0 0 1.5em 0;
  }

  .hero-cta {
    display: flex;
    gap: 1em;
    justify-content: center;
    flex-wrap: wrap;
  }

  .btn.secondary {
    background-color: transparent;
    border: 2px solid #FF8F40;
    color: #FF8F40;
  }

  .btn.secondary:hover {
    background-color: #FF8F40;
    color: #0F1419;
  }

  .featured-projects,
  .latest-posts {
    margin: 3em 0;
  }

  .featured-projects h2,
  .latest-posts h2 {
    color: #FFB454;
    margin-bottom: 1.5em;
  }

  .projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 1.5em;
    margin-bottom: 2em;
  }

  .project-card {
    background-color: rgba(15, 20, 25, 0.5);
    border: 1px solid #626A73;
    border-radius: 8px;
    padding: 1.5em;
    transition: all 0.3s ease;
  }

  .project-card:hover {
    border-color: #FF8F40;
    box-shadow: 0 4px 12px rgba(255, 143, 64, 0.2);
    transform: translateY(-4px);
  }

  .project-card h3 {
    margin: 0 0 0.5em 0;
  }

  .project-card h3 a {
    color: #FFB454;
  }

  .project-card p {
    color: #E6E1CF;
    font-size: 0.95em;
    margin: 0.5em 0 1em 0;
  }

  .project-card-tech {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5em;
    margin: 1em 0;
  }

  .read-more {
    color: #39BAE6;
    text-decoration: none;
    transition: all 0.3s ease;
  }

  .read-more:hover {
    color: #FF8F40;
  }

  .posts-list {
    display: flex;
    flex-direction: column;
    gap: 2em;
    margin-bottom: 2em;
  }

  .post-preview {
    background-color: rgba(15, 20, 25, 0.5);
    border: 1px solid #626A73;
    border-radius: 8px;
    padding: 1.5em;
    transition: all 0.3s ease;
  }

  .post-preview:hover {
    border-color: #AAD94C;
    box-shadow: 0 4px 12px rgba(170, 217, 76, 0.2);
  }

  .post-preview h3 {
    margin: 0 0 0.5em 0;
  }

  .post-preview h3 a {
    color: #FFB454;
  }

  .post-preview .post-meta {
    display: flex;
    gap: 1em;
    margin-bottom: 1em;
    flex-wrap: wrap;
  }

  .post-preview p {
    color: #E6E1CF;
    margin: 0.5em 0 1em 0;
  }

  .view-all {
    text-align: center;
  }

  @media (max-width: 768px) {
    .hero-title {
      font-size: 2em;
    }

    .hero-subtitle {
      font-size: 1.1em;
    }

    .hero-cta {
      flex-direction: column;
    }

    .projects-grid {
      grid-template-columns: 1fr;
    }
  }
</style>
