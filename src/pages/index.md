---
layout: ../layouts/AboutLayout.astro
title: "About"
---

<style>
  /* Beautiful, ethereal center-aligned layout */
  .intro-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    min-height: 65vh;
    text-align: center;
    position: relative;
    padding: 2rem;
  }

  /* Very soft ambient glow behind the text to make it feel like an art piece */
  .intro-glow {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 60vw;
    height: 60vw;
    max-width: 500px;
    max-height: 500px;
    background: radial-gradient(circle, var(--accent) 0%, transparent 70%);
    opacity: 0.04;
    z-index: -1;
    pointer-events: none;
    filter: blur(40px);
  }

  /* Entrance animations */
  @keyframes etherealFloat {
    from { opacity: 0; filter: blur(4px); transform: translateY(12px); }
    to { opacity: 1; filter: blur(0); transform: translateY(0); }
  }

  .reveal {
    animation: etherealFloat 1.4s cubic-bezier(0.22, 1, 0.36, 1) forwards;
    opacity: 0;
  }

  .delay-1 { animation-delay: 200ms; }
  .delay-2 { animation-delay: 500ms; }

  /* English citation - pure, unstructured code comment */
  .code-quote {
    font-family: var(--font-app), ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, monospace;
    font-size: 0.8rem;
    color: var(--foreground);
    opacity: 0.35;
    margin-bottom: 4rem;
    letter-spacing: 0.05em;
    font-style: italic;
  }

  .code-quote::before {
    content: "// ";
    opacity: 0.6;
    font-style: normal;
  }

  /* Chinese Typography - Smiley Sans Oblique */
  .intro-title {
    font-family: "Smiley Sans Oblique", "PingFang SC", "Hiragino Sans GB", "Microsoft YaHei", "Noto Sans SC", sans-serif;
    font-size: clamp(2rem, 5vw, 3.5rem);
    font-weight: 400;
    color: var(--foreground);
    letter-spacing: 0.15em;
    margin: 0;
    line-height: 1.2;
    opacity: 0.95;
  }

  :global(html[data-theme="dark"]) .intro-title {
    color: transparent;
    background: linear-gradient(180deg, #fff 0%, #a1a1aa 100%);
    -webkit-background-clip: text;
    background-clip: text;
  }

  .intro-subtitle {
    font-family: "PingFang SC", "Hiragino Sans GB", "Microsoft YaHei", "Noto Sans SC", sans-serif;
    font-size: clamp(1.2rem, 3vw, 1.8rem);
    font-weight: 300;
    color: var(--foreground);
    letter-spacing: 0.25em;
    opacity: 0.45;
    margin: 0;
    margin-top: 3.5rem;
  }
</style>

<div class="intro-container">
  <div class="intro-glow"></div>

  <div class="reveal">
    <div class="code-quote">notes on code, thoughts, and life.</div>
  </div>

  <div class="reveal delay-1">
    <h1 class="intro-title">这是我的博客</h1>
  </div>

  <div class="reveal delay-2">
    <h2 class="intro-subtitle">欢迎随便看看</h2>
  </div>
</div>
