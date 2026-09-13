---
layout: single
title: ""
author_profile: false
permalink: /
---

<style>
.page__title { display: none; }
.page__content { max-width: none; }
.apple-home {
  color: #1d1d1f;
  font-family: -apple-system, BlinkMacSystemFont, "SF Pro Display", "PingFang SC", "Helvetica Neue", Arial, sans-serif;
  letter-spacing: -0.015em;
  margin: -1.2rem auto 2rem;
  max-width: 1120px;
}
.apple-home * { box-sizing: border-box; }
.apple-hero {
  background: #050505;
  border-radius: 32px;
  color: #f5f5f7;
  min-height: 550px;
  overflow: hidden;
  padding: clamp(3rem, 8vw, 6.8rem);
  position: relative;
}
.apple-hero__content { max-width: 710px; position: relative; z-index: 1; }
.apple-eyebrow {
  color: #a9d8ff;
  font-size: .82rem;
  font-weight: 600;
  letter-spacing: .1em;
  margin: 0 0 1.4rem;
  text-transform: uppercase;
}
.apple-hero h1 {
  color: #f5f5f7;
  font-size: clamp(3.4rem, 8vw, 6.7rem);
  font-weight: 700;
  letter-spacing: -.065em;
  line-height: .94;
  margin: 0;
}
.apple-hero h1 span { color: #8ed5ff; }
.apple-lead {
  color: #d2d2d7;
  font-size: clamp(1.05rem, 2vw, 1.32rem);
  line-height: 1.6;
  margin: 2rem 0;
  max-width: 600px;
}
.apple-actions { display: flex; flex-wrap: wrap; gap: .8rem; }
.apple-actions a {
  border-radius: 980px;
  font-size: .98rem;
  font-weight: 500;
  padding: .7rem 1.2rem;
  text-decoration: none;
}
.apple-button { background: #0071e3; color: #fff !important; }
.apple-button:hover { background: #0077ed; }
.apple-button--ghost { background: rgba(255,255,255,.13); color: #fff !important; }
.apple-orb { border-radius: 50%; filter: blur(1px); position: absolute; }
.apple-orb--blue { background: radial-gradient(circle at 35% 35%, #81d4fa 0, #1976d2 35%, rgba(25,118,210,0) 70%); height: 490px; opacity: .85; right: -110px; top: -115px; width: 490px; }
.apple-orb--violet { background: radial-gradient(circle, #8b5cf6 0, rgba(96,58,209,0) 68%); bottom: -210px; height: 550px; opacity: .45; right: 20%; width: 550px; }
.apple-section { padding: 6rem 1.2rem 0; }
.apple-heading { font-size: clamp(2.3rem, 5vw, 4rem); font-weight: 700; letter-spacing: -.055em; line-height: 1.04; margin: 0 0 .7rem; }
.apple-subhead { color: #6e6e73; font-size: 1.08rem; line-height: 1.55; margin: 0 0 2rem; max-width: 570px; }
.apple-grid { display: grid; gap: 1rem; grid-template-columns: repeat(2, minmax(0, 1fr)); }
.apple-card {
  background: #f5f5f7;
  border-radius: 24px;
  min-height: 235px;
  padding: 2rem;
}
.apple-card--blue { background: linear-gradient(135deg, #e9f6ff, #d9ecff); }
.apple-card--warm { background: linear-gradient(135deg, #fff5e8, #fde7cc); }
.apple-card__number { color: #0071e3; font-size: .85rem; font-weight: 700; letter-spacing: .08em; }
.apple-card h3 { font-size: 1.55rem; letter-spacing: -.04em; line-height: 1.12; margin: .7rem 0; }
.apple-card p { color: #515154; line-height: 1.55; margin: 0; }
.apple-timeline { border-top: 1px solid #d2d2d7; }
.apple-timeline__item { border-bottom: 1px solid #d2d2d7; display: grid; gap: 1rem; grid-template-columns: 120px 1fr; padding: 1.5rem 0; }
.apple-timeline__year { color: #6e6e73; font-size: .95rem; }
.apple-timeline h3 { font-size: 1.22rem; letter-spacing: -.025em; margin: 0 0 .25rem; }
.apple-timeline p { color: #6e6e73; margin: 0; }
.apple-projects { display: grid; gap: 1rem; grid-template-columns: repeat(2, minmax(0, 1fr)); }
.apple-project {
  background: #101010;
  border-radius: 24px;
  color: #f5f5f7;
  min-height: 310px;
  padding: 2rem;
}
.apple-project:nth-child(2) { background: #1d2632; }
.apple-project__tag { color: #8ed5ff; font-size: .82rem; font-weight: 600; letter-spacing: .08em; text-transform: uppercase; }
.apple-project h3 { color: #fff; font-size: 1.75rem; letter-spacing: -.045em; line-height: 1.08; margin: .75rem 0; }
.apple-project p { color: #d2d2d7; line-height: 1.6; }
.apple-contact { padding-bottom: 2rem; text-align: center; }
.apple-contact__panel { background: linear-gradient(135deg, #eef7ff, #f5f0ff); border-radius: 28px; padding: clamp(2.4rem, 6vw, 4.5rem) 1.5rem; }
.apple-contact h2 { font-size: clamp(2.4rem, 5vw, 4.2rem); letter-spacing: -.06em; line-height: 1; margin: 0 0 1rem; }
.apple-contact p { color: #515154; font-size: 1.08rem; margin: 0 0 1.6rem; }
.apple-contact a { background: #0071e3; border-radius: 980px; color: #fff !important; display: inline-block; padding: .75rem 1.3rem; text-decoration: none; }
.apple-note { color: #86868b; font-size: .78rem; margin-top: 2rem; }
@media (max-width: 650px) {
  .apple-home { margin-top: -.7rem; }
  .apple-hero { border-radius: 24px; min-height: 500px; padding: 3.5rem 1.8rem; }
  .apple-section { padding: 4rem 0 0; }
  .apple-grid, .apple-projects { grid-template-columns: 1fr; }
  .apple-timeline__item { grid-template-columns: 1fr; gap: .35rem; }
  .apple-orb--blue { right: -250px; top: -70px; }
}
</style>

<div class="apple-home">

<section class="apple-hero">
  <div class="apple-orb apple-orb--blue"></div>
  <div class="apple-orb apple-orb--violet"></div>
  <div class="apple-hero__content">
    <p class="apple-eyebrow">Digital Marketing & Communication</p>
    <h1>洞察连接<br><span>人与品牌。</span></h1>
    <p class="apple-lead">我是徐昕哲，南京大学新闻传播学院新闻与传播硕士研究生。关注数字平台、品牌传播与消费者之间不断变化的关系。</p>
    <div class="apple-actions">
      <a class="apple-button" href="/portfolio/">浏览研究与项目</a>
      <a class="apple-button--ghost" href="/cv/">查看个人简历</a>
    </div>
  </div>
</section>

<section class="apple-section">
  <h2 class="apple-heading">研究，让沟通更有意义。</h2>
  <p class="apple-subhead">从内容策略到用户互动，我尝试在数据、创意与社会语境之间建立更清晰的理解。</p>
  <div class="apple-grid">
    <article class="apple-card apple-card--blue">
      <div class="apple-card__number">01 / BRAND</div>
      <h3>数字营销与<br>品牌传播</h3>
      <p>关注品牌如何在数字环境中建立有意义、可持续的连接。</p>
    </article>
    <article class="apple-card apple-card--warm">
      <div class="apple-card__number">02 / PLATFORM</div>
      <h3>社交媒体与<br>平台传播</h3>
      <p>探索平台机制、内容流动与用户互动之间的关系。</p>
    </article>
    <article class="apple-card">
      <div class="apple-card__number">03 / PEOPLE</div>
      <h3>消费者洞察与<br>用户互动</h3>
      <p>从用户行为和反馈中理解需求、态度与决策过程。</p>
    </article>
    <article class="apple-card">
      <div class="apple-card__number">04 / DATA</div>
      <h3>数据驱动的<br>内容策略</h3>
      <p>尝试用数据支持内容优化与传播效果评估。</p>
    </article>
  </div>
</section>

<section class="apple-section">
  <h2 class="apple-heading">学习轨迹。</h2>
  <div class="apple-timeline">
    <div class="apple-timeline__item">
      <div class="apple-timeline__year">2026 — 至今</div>
      <div><h3>南京大学新闻传播学院</h3><p>新闻与传播硕士研究生</p></div>
    </div>
    <div class="apple-timeline__item">
      <div class="apple-timeline__year">2022 — 2026</div>
      <div><h3>南京师范大学新闻传播学院</h3><p>广告学本科生</p></div>
    </div>
  </div>
</section>

<section class="apple-section">
  <h2 class="apple-heading">课程项目。</h2>
  <p class="apple-subhead">从研究问题出发，尝试将分析转化为可被讨论的传播洞察。</p>
  <div class="apple-projects">
    <article class="apple-project">
      <div class="apple-project__tag">Course Project 01</div>
      <h3>社交媒体<br>品牌传播分析</h3>
      <p>以某消费品牌为案例，梳理内容策略、用户互动方式与传播效果，并尝试形成可执行的内容优化建议。</p>
    </article>
    <article class="apple-project">
      <div class="apple-project__tag">Course Project 02</div>
      <h3>数字平台<br>用户洞察</h3>
      <p>结合公开数据、问卷或访谈材料，分析数字平台用户的内容偏好与消费决策过程。</p>
    </article>
  </div>
</section>

<section class="apple-section apple-contact">
  <div class="apple-contact__panel">
    <h2>保持好奇，<br>持续连接。</h2>
    <p>欢迎就数字营销传播、平台研究与内容策略交流。</p>
    <a href="mailto:Lemcous@163.com">发送邮件</a>
    <div class="apple-note">本个人网站用于计算传播学导论课程作业展示。</div>
  </div>
</section>

</div>
