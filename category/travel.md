---
layout: default
title: 여행 카테고리
description: 캠핑, 제주도, 등산 등 여행 정보
category: travel
---

<main class="container">
  <section class="hero" style="background: linear-gradient(135deg, #06b6d4 0%, #0891b2 100%);">
    <h1>✈️ 여행</h1>
    <p>캠핑, 제주도, 등산 등 여행 관련 정보와 추천 코스를 제공합니다.</p>
  </section>

  <section class="trending">
    <div class="section-header">
      <h2>🏔️ 여행 정보</h2>
    </div>
    <div class="grid">
      {% assign category_posts = site.posts | where: "category", "travel" | default: site.posts %}
      {% for post in category_posts limit: 12 %}
      <article class="post-card">
        <span class="category-tag" style="background: #06b6d4;">여행</span>
        <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
        <p>{{ post.description | default: '여행 관련 정보입니다.' }}</p>
        <div class="meta">
          <span>📅 {{ post.date | date: '%Y.%m.%d' }}</span>
        </div>
      </article>
      {% endfor %}
    </div>
  </section>
</main>