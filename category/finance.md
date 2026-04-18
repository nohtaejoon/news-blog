---
layout: default
title: 금융 카테고리
description: 금 시세, ETF, 비트코인 등 금융 투자의 심층 분석
category: finance
---

<main class="container">
  <section class="hero" style="background: linear-gradient(135deg, #10b981 0%, #059669 100%);">
    <h1>💰 금융 투자</h1>
    <p>금 시세, ETF, 비트코인 등 금융 투자의 심층 분석과 투자 전략을 제공합니다.</p>
  </section>

  <section class="trending">
    <div class="section-header">
      <h2>📈 금융 투자 분석</h2>
    </div>
    <div class="grid">
      {% assign category_posts = site.posts | where: "category", "finance" | default: site.posts %}
      {% for post in category_posts limit: 12 %}
      <article class="post-card">
        <span class="category-tag" style="background: #10b981;">금융</span>
        <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
        <p>{{ post.description | default: '금융 투자 관련 심층 분석 기사입니다.' }}</p>
        <div class="meta">
          <span>📅 {{ post.date | date: '%Y.%m.%d' }}</span>
        </div>
      </article>
      {% endfor %}
    </div>
  </section>
</main>