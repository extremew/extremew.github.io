---
title: Learning Journey
layout: page
permalink: /learning/
---

# 📚 My Learning Journey

A collection of blog posts documenting my continuous learning experiences, technical discoveries, and insights from building projects.

<div class="posts-container">
  {% for post in site.posts %}
    <article class="blog-item">
      <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
      <div class="blog-meta">
        <span class="post-date">📅 {{ post.date | date: "%B %d, %Y" }}</span>
        {% if post.categories %}
          <div class="post-categories">
            {% for category in post.categories %}
              <span class="badge">{{ category }}</span>
            {% endfor %}
          </div>
        {% endif %}
      </div>
      <p>{{ post.excerpt | strip_html | truncatewords: 50 }}</p>
      <a href="{{ post.url }}" class="read-more">Read Full Post →</a>
    </article>
  {% endfor %}
</div>

<style>
  .posts-container {
    display: flex;
    flex-direction: column;
    gap: 2em;
    margin-top: 2em;
  }

  .blog-item {
    background-color: rgba(15, 20, 25, 0.5);
    border: 1px solid #626A73;
    border-radius: 8px;
    padding: 1.5em;
    transition: all 0.3s ease;
  }

  .blog-item:hover {
    border-color: #AAD94C;
    box-shadow: 0 4px 12px rgba(170, 217, 76, 0.2);
  }

  .blog-item h3 {
    margin: 0 0 0.75em 0;
  }

  .blog-item h3 a {
    color: #FFB454;
  }

  .blog-meta {
    display: flex;
    gap: 1em;
    align-items: center;
    flex-wrap: wrap;
    margin-bottom: 1em;
    color: #626A73;
    font-size: 0.95em;
  }

  .blog-item p {
    color: #E6E1CF;
    margin: 0.5em 0 1em 0;
  }
</style>
