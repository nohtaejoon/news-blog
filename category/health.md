---
layout: default
title: 건강 카테고리
description: 홈트레이닝, 프로틴, 마라톤 등 건강 피트니스 정보
category: health
---

<main class="container">
  <section class="hero" style="background: linear-gradient(135deg, #f59e0b 0%, #d97706 100%);">
    <h1>💪 건강 피트니스</h1>
    <p>홈트레이닝, 프로틴 섭취, 마라톤 준비 등 건강 피트니스 정보를 제공합니다.</p>
  </section>

  <section class="trending">
    <div class="section-header">
      <h2>🏃 건강 피트니스</h2>
    </div>
    <div class="grid">
      {% assign category_posts = site.posts | where: "category", "health" | default: site.posts %}
      {% for post in category_posts limit: 12 %}
      <article class="post-card">
        <span class="category-tag" style="background: #f59e0b;">건강</span>
        <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
        <p>{{ post.description | default: '건강 피트니스 관련 정보입니다.' }}</p>
        <div class="meta">
          <span>📅 {{ post.date | date: '%Y.%m.%d' }}</span>
        </div>
      </article>
      {% endfor %}
    </div>
  </section>
</main>