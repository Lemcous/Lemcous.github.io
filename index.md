---
layout: single
title: "关于我"
author_profile: true
---

<style>
.page__title { display: none; }

.about-vibe {
  --ink: #1d1d1f;
  --mist-green: #e5f2ed;
  --mist-blue: #eaf4f8;
  --accent: #4f7f82;
  --paper: rgba(255, 255, 255, .72);
  color: var(--ink);
  font-size: 16px;
  margin-top: -.3rem;
}

.about-vibe p { max-width: none; }

.av-shell {
  background:
    radial-gradient(circle at 80% 18%, rgba(255,255,255,.52) 0 1px, transparent 2px),
    radial-gradient(circle at 16% 77%, rgba(255,255,255,.42) 0 1px, transparent 2px),
    linear-gradient(135deg, #e7f3ee 0%, #eaf4f8 52%, #dfeef0 100%);
  border-radius: 28px;
  overflow: hidden;
  padding: clamp(1rem, 2.8vw, 2rem);
  position: relative;
}

.av-shell::before,
.av-shell::after {
  border: 1px solid rgba(255,255,255,.5);
  border-radius: 50%;
  content: "";
  pointer-events: none;
  position: absolute;
}

.av-shell::before { height: 3rem; right: 13%; top: 21%; width: 3rem; }
.av-shell::after { bottom: 9%; height: 1.5rem; left: 52%; width: 1.5rem; }

.av-nav {
  align-items: center;
  backdrop-filter: blur(12px);
  background: rgba(255,255,255,.70);
  border: 1px solid rgba(255,255,255,.88);
  border-radius: 999px;
  display: flex;
  gap: 1rem;
  justify-content: space-between;
  margin: 0 auto;
  max-width: 52rem;
  padding: .5rem .65rem .5rem 1rem;
  position: relative;
  z-index: 2;
}

.av-brand {
  align-items: center;
  display: flex;
  font-size: 12px;
  font-weight: 800;
  gap: .5rem;
  letter-spacing: .06em;
}

.av-brand__mark {
  align-items: center;
  background: var(--ink);
  border-radius: 50%;
  color: #fff;
  display: inline-flex;
  font-size: 9px;
  height: 1.35rem;
  justify-content: center;
  width: 1.35rem;
}

.av-nav__links { display: flex; gap: .1rem; }
.av-nav__links a {
  border-radius: 999px;
  color: #524b51;
  font-size: 12px;
  padding: .43rem .7rem;
  text-decoration: none;
  transition: background-color .25s ease, color .25s ease;
}
.av-nav__links a:hover { background: rgba(255,255,255,.85); color: var(--ink); }

.av-hero {
  align-items: center;
  display: grid;
  gap: clamp(1.4rem, 4vw, 3.6rem);
  grid-template-columns: minmax(0, 1.05fr) minmax(15rem, .95fr);
  min-height: 35rem;
  padding: clamp(2rem, 5vw, 5.4rem) clamp(.4rem, 2vw, 2rem) 2rem;
  position: relative;
  z-index: 1;
}

.av-copy { padding-left: clamp(0rem, 2vw, 1.2rem); }

.av-eyebrow {
  align-items: center;
  color: #557075;
  display: flex;
  font-size: 11px;
  font-weight: 800;
  gap: .35rem;
  letter-spacing: .1em;
  margin: 0 0 1rem;
}
.av-eyebrow::before { background: #67a99d; border-radius: 50%; content: ""; height: .42rem; width: .42rem; }

.av-name {
  font-size: clamp(3.1rem, 6.8vw, 6rem);
  font-weight: 850;
  letter-spacing: -.1em;
  line-height: .92;
  margin: 0;
}
.av-name span { display: block; }

.av-role {
  color: var(--accent);
  font-size: clamp(1rem, 1.8vw, 1.3rem);
  font-weight: 700;
  letter-spacing: -.04em;
  margin: 1rem 0 1.1rem;
}

.av-intro {
  color: #4f6267;
  font-size: 14px;
  line-height: 1.8;
  margin: 0;
  max-width: 29rem;
}

.av-chips { display: flex; flex-wrap: wrap; gap: .5rem; margin-top: 1.2rem; }
.av-chip {
  background: rgba(255,255,255,.62);
  border: 1px solid rgba(255,255,255,.76);
  border-radius: 999px;
  color: #4d6568;
  font-size: 12px;
  padding: .38rem .7rem;
}

.av-actions { display: flex; flex-wrap: wrap; gap: .6rem; margin-top: 1.35rem; }
.av-button {
  border-radius: 999px;
  font-size: 13px;
  font-weight: 750;
  padding: .67rem 1rem;
  text-decoration: none;
  transition: transform .26s cubic-bezier(.22,1,.36,1), box-shadow .26s ease;
}
.av-button:hover { transform: translateY(-3px) rotate(-1deg); }
.av-button--dark { background: var(--ink); box-shadow: 0 8px 16px rgba(28,22,25,.16); color: #fff; }
.av-button--paper { background: var(--paper); border: 1px solid rgba(255,255,255,.9); color: var(--ink); }

.av-portrait-zone { min-height: 27rem; position: relative; }
.av-portrait-backdrop {
  background: linear-gradient(145deg, #b7dcd6, #9fcad1);
  border-radius: 44% 56% 43% 57% / 43% 47% 53% 57%;
  height: min(27rem, 47vw);
  left: 50%;
  overflow: hidden;
  position: absolute;
  top: 50%;
  transform: translate(-50%, -50%) rotate(-5deg);
  width: min(20rem, 82%);
}
.av-portrait-backdrop::after {
  border: 1px solid rgba(255,255,255,.35);
  border-radius: 50%;
  content: "";
  height: 3.5rem;
  position: absolute;
  right: 1.6rem;
  top: 2rem;
  width: 3.5rem;
}
.av-portrait {
  bottom: 0;
  filter: drop-shadow(0 16px 18px rgba(63, 103, 106, .18));
  height: 92%;
  left: 50%;
  object-fit: cover;
  object-position: center top;
  position: absolute;
  transform: translateX(-50%);
  width: 82%;
}
.av-note {
  background: rgba(255,255,255,.86);
  border: 1px solid rgba(255,255,255,.95);
  border-radius: 14px;
  bottom: 1.2rem;
  box-shadow: 0 10px 20px rgba(65,49,54,.1);
  color: #4d6568;
  font-size: 12px;
  line-height: 1.45;
  padding: .65rem .75rem;
  position: absolute;
  right: -.15rem;
  transform: rotate(4deg);
  width: 9.8rem;
}
.av-note strong { color: var(--ink); display: block; font-size: 11px; margin-bottom: .2rem; }

.av-strip {
  display: grid;
  gap: .75rem;
  grid-template-columns: repeat(3, 1fr);
  margin-top: .6rem;
  position: relative;
  z-index: 1;
}
.av-strip__item {
  background: rgba(255,255,255,.48);
  border: 1px solid rgba(255,255,255,.72);
  border-radius: 15px;
  min-height: 5.8rem;
  padding: .85rem;
  transition: transform .3s cubic-bezier(.22,1,.36,1), background-color .3s ease;
}
.av-strip__item:hover { background: rgba(255,255,255,.72); transform: translateY(-5px); }
.av-strip__label { color: #6c6268; font-size: 11px; font-weight: 800; letter-spacing: .08em; margin: 0 0 .45rem; }
.av-strip__value { font-size: 14px; font-weight: 750; line-height: 1.45; margin: 0; }

.av-shell.is-visible .av-nav { animation: av-up .65s cubic-bezier(.22,1,.36,1) both; }
.av-shell.is-visible .av-copy { animation: av-up .8s .08s cubic-bezier(.22,1,.36,1) both; }
.av-shell.is-visible .av-portrait-zone { animation: av-pop .8s .18s cubic-bezier(.22,1,.36,1) both; }
.av-shell.is-visible .av-strip { animation: av-up .75s .26s cubic-bezier(.22,1,.36,1) both; }
@keyframes av-up { from { opacity: 0; transform: translateY(20px); } to { opacity: 1; transform: translateY(0); } }
@keyframes av-pop { from { opacity: 0; transform: scale(.94) rotate(2deg); } to { opacity: 1; transform: scale(1) rotate(0); } }

@media (max-width: 48em) {
  .av-nav__links a:not(:last-child) { display: none; }
  .av-hero { grid-template-columns: 1fr; min-height: auto; padding-top: 3rem; }
  .av-portrait-zone { min-height: 22rem; }
  .av-portrait-backdrop { height: 21rem; width: 16rem; }
  .av-name { font-size: clamp(3.1rem, 16vw, 4.8rem); }
}
@media (max-width: 32em) {
  .av-shell { border-radius: 20px; padding: .75rem; }
  .av-strip { grid-template-columns: 1fr; }
  .av-nav { padding-left: .75rem; }
}
@media (prefers-reduced-motion: reduce) {
  .av-shell *, .av-shell *::before, .av-shell *::after { animation: none !important; transition: none !important; }
}
</style>

<div class="about-vibe">
  <div class="av-shell">
    <nav class="av-nav">
      <div class="av-brand"><span class="av-brand__mark">XZ</span> XINZHE / PORTFOLIO</div>
      <div class="av-nav__links">
        <a href="/cv/">个人简历</a>
        <a href="/works/">个人作品集</a>
      </div>
    </nav>

    <section class="av-hero">
      <div class="av-copy">
        <p class="av-eyebrow">HELLO / 你好</p>
        <h1 class="av-name"><span>Hi,</span><span>我是徐昕哲</span></h1>
        <p class="av-role">Digital Marketing / 内容传播</p>
        <p class="av-intro">南京大学新闻传播学院新闻与传播硕士研究生。关注数字平台、内容策略与品牌沟通，希望用研究与实践理解内容如何真正影响用户。</p>
        <div class="av-chips">
          <span class="av-chip">品牌传播</span>
          <span class="av-chip">用户洞察</span>
          <span class="av-chip">内容策略</span>
        </div>
        <div class="av-actions">
          <a class="av-button av-button--dark" href="/cv/">了解我的经历</a>
          <a class="av-button av-button--paper" href="/works/">查看作品集</a>
        </div>
      </div>

      <div class="av-portrait-zone">
        <div class="av-portrait-backdrop">
          <img class="av-portrait" src="/images/IMG_8580.JPG" alt="徐昕哲">
        </div>
        <div class="av-note"><strong>CURRENTLY</strong>在南京学习数字营销传播，也在慢慢搭建自己的作品集。</div>
      </div>
    </section>

    <section class="av-strip">
      <article class="av-strip__item">
        <p class="av-strip__label">NOW STUDYING</p>
        <p class="av-strip__value">新闻与传播<br>数字营销传播方向</p>
      </article>
      <article class="av-strip__item">
        <p class="av-strip__label">INTERESTED IN</p>
        <p class="av-strip__value">社交媒体 · 用户研究<br>品牌内容策略</p>
      </article>
      <article class="av-strip__item">
        <p class="av-strip__label">BASED IN</p>
        <p class="av-strip__value">南京，中国<br>欢迎通过邮箱联系</p>
      </article>
    </section>
  </div>
</div>

<script>
document.querySelector('.av-shell')?.classList.add('is-visible');
</script>
