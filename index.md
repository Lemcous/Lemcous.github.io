---
layout: single
title: "关于我"
author_profile: true
---

<style>
.about-vibe {
  --av-ink: #172033;
  --av-muted: #61708a;
  --av-blue: #3d6df2;
  --av-sky: #eaf1ff;
  --av-line: #dbe4f5;
  color: var(--av-ink);
  font-size: 16px;
}

.about-vibe p { max-width: none; }

.about-vibe .av-hero {
  background: linear-gradient(135deg, #e8f0ff 0%, #f7faff 48%, #e7fbf7 100%);
  border: 1px solid #d9e6ff;
  border-radius: 24px;
  overflow: hidden;
  padding: clamp(1.5rem, 4vw, 3.1rem);
  position: relative;
}

.about-vibe .av-hero::after {
  background: rgba(61, 109, 242, .1);
  border-radius: 50%;
  content: "";
  height: 13rem;
  position: absolute;
  right: -4rem;
  top: -5rem;
  width: 13rem;
}

.about-vibe .av-eyebrow,
.about-vibe .av-label {
  color: var(--av-blue);
  font-size: 12px;
  font-weight: 800;
  letter-spacing: .12em;
  margin: 0 0 .7rem;
  text-transform: uppercase;
}

.about-vibe .av-name {
  font-size: clamp(2.3rem, 6vw, 4.4rem);
  font-weight: 800;
  letter-spacing: -.075em;
  line-height: 1;
  margin: 0;
  position: relative;
  z-index: 1;
}

.about-vibe .av-tagline {
  color: #34415a;
  font-size: clamp(1rem, 2vw, 1.22rem);
  line-height: 1.75;
  margin: 1rem 0 0;
  max-width: 34rem;
  position: relative;
  z-index: 1;
}

.about-vibe .av-status {
  align-items: center;
  background: rgba(255,255,255,.7);
  border: 1px solid rgba(255,255,255,.9);
  border-radius: 999px;
  color: #43516c;
  display: inline-flex;
  font-size: 14px;
  gap: .5rem;
  margin-top: 1.35rem;
  padding: .48rem .85rem;
  position: relative;
  z-index: 1;
}

.about-vibe .av-dot {
  background: #1aa77a;
  border-radius: 50%;
  box-shadow: 0 0 0 4px rgba(26,167,122,.12);
  height: .5rem;
  width: .5rem;
}

.about-vibe .av-actions {
  display: flex;
  flex-wrap: wrap;
  gap: .65rem;
  margin-top: 1.5rem;
  position: relative;
  z-index: 1;
}

.about-vibe .av-button {
  border-radius: 999px;
  font-size: 14px;
  font-weight: 700;
  padding: .62rem 1rem;
  text-decoration: none;
}

.about-vibe .av-button--primary {
  background: var(--av-ink);
  color: #fff;
}

.about-vibe .av-button--secondary {
  background: rgba(255,255,255,.66);
  border: 1px solid #d1ddf5;
  color: var(--av-ink);
}

.about-vibe .av-section {
  margin-top: 2.25rem;
}

.about-vibe .av-section__head {
  align-items: baseline;
  display: flex;
  gap: .75rem;
  justify-content: space-between;
  margin-bottom: .85rem;
}

.about-vibe .av-section__title {
  border: 0;
  font-size: 21px;
  letter-spacing: -.035em;
  margin: 0;
  padding: 0;
}

.about-vibe .av-section__note {
  color: var(--av-muted);
  font-size: 13px;
  margin: 0;
}

.about-vibe .av-grid {
  display: grid;
  gap: .85rem;
  grid-template-columns: repeat(3, minmax(0, 1fr));
}

.about-vibe .av-card {
  background: #fff;
  border: 1px solid var(--av-line);
  border-radius: 16px;
  min-height: 11rem;
  padding: 1.1rem;
}

.about-vibe .av-card--feature {
  background: var(--av-ink);
  border-color: var(--av-ink);
  color: #fff;
}

.about-vibe .av-card--feature .av-label,
.about-vibe .av-card--feature .av-card__text {
  color: rgba(255,255,255,.7);
}

.about-vibe .av-card__title {
  font-size: 17px;
  letter-spacing: -.025em;
  line-height: 1.35;
  margin: 0 0 .6rem;
}

.about-vibe .av-card__text {
  color: var(--av-muted);
  font-size: 14px;
  line-height: 1.65;
  margin: 0;
}

.about-vibe .av-timeline {
  display: grid;
  gap: .7rem;
}

.about-vibe .av-timeline__item {
  align-items: center;
  border-bottom: 1px solid var(--av-line);
  display: grid;
  gap: .75rem;
  grid-template-columns: 6rem minmax(0, 1fr);
  padding: .75rem 0;
}

.about-vibe .av-timeline__date {
  color: var(--av-blue);
  font-size: 13px;
  font-weight: 700;
}

.about-vibe .av-timeline__main {
  font-size: 15px;
  line-height: 1.5;
}

.about-vibe .av-timeline__main span {
  color: var(--av-muted);
  font-size: 14px;
}

@media (max-width: 40em) {
  .about-vibe .av-grid { grid-template-columns: 1fr; }
  .about-vibe .av-card { min-height: auto; }
  .about-vibe .av-section__head { align-items: flex-start; flex-direction: column; gap: .3rem; }
  .about-vibe .av-timeline__item { grid-template-columns: 1fr; gap: .2rem; }
}
</style>

<div class="about-vibe">

  <section class="av-hero">
    <p class="av-eyebrow">Hello, I am</p>
    <h2 class="av-name">徐昕哲</h2>
    <p class="av-tagline">南京大学新闻传播学院新闻与传播硕士研究生。关注数字平台、内容策略与品牌如何建立更有效的沟通。</p>
    <div class="av-status"><span class="av-dot"></span>目前在南京 · 持续积累研究与传播实践</div>
    <div class="av-actions">
      <a class="av-button av-button--primary" href="/cv/">查看个人简历</a>
      <a class="av-button av-button--secondary" href="/works/">浏览个人作品集</a>
    </div>
  </section>

  <section class="av-section">
    <div class="av-section__head">
      <h2 class="av-section__title">我关心什么</h2>
      <p class="av-section__note">Focus areas</p>
    </div>
    <div class="av-grid">
      <article class="av-card av-card--feature">
        <p class="av-label">01 / Brand</p>
        <h3 class="av-card__title">数字营销与品牌传播</h3>
        <p class="av-card__text">从传播目标、内容表达与用户反馈，理解品牌在数字环境中的沟通方式。</p>
      </article>
      <article class="av-card">
        <p class="av-label">02 / Platform</p>
        <h3 class="av-card__title">社交媒体与平台传播</h3>
        <p class="av-card__text">关注平台机制、内容形态与互动行为之间的关系。</p>
      </article>
      <article class="av-card">
        <p class="av-label">03 / Audience</p>
        <h3 class="av-card__title">消费者洞察</h3>
        <p class="av-card__text">理解用户需求、使用场景与消费决策如何被内容影响。</p>
      </article>
    </div>
  </section>

  <section class="av-section">
    <div class="av-section__head">
      <h2 class="av-section__title">现在在做什么</h2>
      <p class="av-section__note">Now</p>
    </div>
    <div class="av-timeline">
      <div class="av-timeline__item">
        <div class="av-timeline__date">2026 — 至今</div>
        <div class="av-timeline__main">南京大学新闻传播学院 <span>· 新闻与传播硕士研究生，数字营销传播方向</span></div>
      </div>
      <div class="av-timeline__item">
        <div class="av-timeline__date">研究训练</div>
        <div class="av-timeline__main">用户研究与内容分析 <span>· 问卷、访谈、SPSS 数据处理与研究汇报</span></div>
      </div>
      <div class="av-timeline__item">
        <div class="av-timeline__date">实践积累</div>
        <div class="av-timeline__main">传播与运营 <span>· 内容策划、项目协作、活动影像记录</span></div>
      </div>
    </div>
  </section>

</div>
