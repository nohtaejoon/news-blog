---
layout: default
title: IT/테크 카테고리
description: AI, 코딩, 맥북 등 IT/테크 관련 최신 정보와 분석
category: it
---

<main class="container">
  <section class="hero" style="background: linear-gradient(135deg, #2563eb 0%, #7c3aed 100%);">
    <h1>💻 IT/테크</h1>
    <p>AI, 코딩, 맥북, 챗GPT 등 IT/테크 분야의 심층 분석과 의견을 제공합니다.</p>
  </section>

  <section class="trending">
    <div class="section-header">
      <h2>📰 IT/테크 최신 분석</h2>
    </div>
    <div class="grid">
      {% assign category_posts = site.posts | where: "category", "it" | default: site.posts %}
      {% for post in category_posts limit: 12 %}
      <article class="post-card">
        <span class="category-tag" style="background: #2563eb;">IT</span>
        <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
        <p>{{ post.description | default: 'IT/테크 관련 심층 분석 기사입니다.' }}</p>
        <div class="meta">
          <span>📅 {{ post.date | date: '%Y.%m.%d' }}</span>
        </div>
      </article>
      {% endfor %}
    </div>
  </section>
</main>