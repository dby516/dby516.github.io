---
permalink: /
title: ""
author_profile: true
header:
  overlay_image: landscape.jpg
  overlay_filter: "rgba(0, 0, 0, 0)"
  typewriter_text: "robotics / trustworthy_autonomy / generalizable_learning"
redirect_from:
  - /about/
  - /about.html
---

<style>
.masthead {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  width: 100%;
  border-bottom: 0;
  background: transparent;
  box-shadow: none;
}

.masthead__inner-wrap {
  text-shadow: 0 2px 12px rgba(0, 0, 0, 0.45);
}

.greedy-nav {
  background: transparent;
}

.greedy-nav a,
.greedy-nav a:visited,
.greedy-nav .visible-links a,
.masthead__menu-item a {
  color: #fff;
}

.greedy-nav a:hover,
.greedy-nav .visible-links a:hover {
  color: #9ee7ff;
}

.greedy-nav button {
  background: rgba(0, 0, 0, 0.18);
}

.greedy-nav .navicon,
.greedy-nav .navicon::before,
.greedy-nav .navicon::after {
  background: #fff;
}

.greedy-nav .hidden-links {
  background: rgba(15, 23, 42, 0.94);
  border-color: rgba(255, 255, 255, 0.18);
}

.page__hero--overlay {
  min-height: 240px;
  margin-bottom: 2.5rem;
  padding: 0;
  background-position: center;
}

.page__hero--overlay::before {
  content: "";
  position: absolute;
  inset: 0;
  pointer-events: none;
  background: linear-gradient(90deg, rgba(0, 0, 0, 0.58) 0%, rgba(0, 0, 0, 0.36) 38%, rgba(0, 0, 0, 0.08) 68%, rgba(0, 0, 0, 0) 100%);
}

.page__hero--overlay .wrapper {
  position: relative;
  min-height: 240px;
}

.page__hero--overlay .page__title,
.page__hero--overlay .page__lead {
  display: none;
}

.page__hero-typewriter {
  position: absolute;
  left: 1rem;
  right: 1rem;
  bottom: 2rem;
  max-width: 980px;
  font-family: "SFMono-Regular", "Consolas", monospace;
  color: #9ee7ff;
  font-size: 0.98rem;
  line-height: 1.5;
  letter-spacing: 0.03em;
  text-shadow: 0 2px 16px rgba(0, 0, 0, 0.45);
  overflow-wrap: anywhere;
}

.cursor {
  animation: blink 1s infinite;
}

.page__content {
  padding-top: 0;
  margin-top: 0;
  background: #fff;
}

.page__content h1 {
  margin-top: 3.5rem;
}

.page__content h1:first-child {
  margin-top: 0;
}

#news {
  margin-top: 3rem;
}

#projects,
#teaching {
  padding-top: 1rem;
}

@keyframes blink {
  0%, 50% { opacity: 1; }
  51%, 100% { opacity: 0; }
}

@media (min-width: 80em) {
  .page__hero--overlay,
  .page__hero--overlay .wrapper {
    min-height: 280px;
  }
}

@media (max-width: 600px) {
  .page__hero--overlay,
  .page__hero--overlay .wrapper {
    min-height: 180px;
  }

  .page__hero-typewriter {
    bottom: 1rem;
    font-size: 0.78rem;
    line-height: 1.45;
  }

  .page__content h1 {
    margin-top: 2.5rem;
  }
}
.research-keyword {
  font-weight: 600;
  color: #1f6f8b;
}
.cursor-orbit {
  position: fixed;
  left: 0;
  top: 0;
  width: 180px;
  height: 180px;
  pointer-events: none;
  z-index: 9999;
  opacity: 0;
  transform: translate3d(-50%, -50%, 0);
  transition: opacity 0.18s ease;
  box-shadow: 0 0 22px rgba(14, 165, 233, 0.22);
}

.cursor-orbit::before,
.cursor-orbit::after {
  content: "";
  position: absolute;
  border-radius: 999px;
  background: radial-gradient(circle, rgba(14, 165, 233, 0.42), rgba(14, 165, 233, 0.14) 42%, transparent 70%);
}

.cursor-orbit::before {
  width: 42px;
  height: 42px;
  left: 28px;
  top: 36px;
  animation: cursorOrbitA 3.2s linear infinite;
}

.cursor-orbit::after {
  width: 24px;
  height: 24px;
  right: 34px;
  bottom: 42px;
  animation: cursorOrbitB 4.4s linear infinite;
}

.cursor-ripple {
  position: fixed;
  width: 12px;
  height: 12px;
  border: 1px solid rgba(14, 165, 233, 0.82);
  border-radius: 999px;
  pointer-events: none;
  z-index: 10000;
  transform: translate(-50%, -50%) scale(1);
  animation: cursorRipple 0.7s ease-out forwards;
  box-shadow: 0 0 22px rgba(14, 165, 233, 0.22);
}

@keyframes cursorOrbitA {
  from { transform: rotate(0deg) translateX(10px) rotate(0deg); }
  to { transform: rotate(360deg) translateX(10px) rotate(-360deg); }
}

@keyframes cursorOrbitB {
  from { transform: rotate(360deg) translateX(8px) rotate(-360deg); }
  to { transform: rotate(0deg) translateX(8px) rotate(0deg); }
}

@keyframes cursorRipple {
  to {
    opacity: 0;
    transform: translate(-50%, -50%) scale(7);
  }
}

@media (hover: none), (pointer: coarse), (prefers-reduced-motion: reduce) {
  .cursor-orbit,
  .cursor-ripple {
    display: none;
  }
}
</style>

<script>
(function () {
  const target = document.getElementById("typed-text");
  const source = document.querySelector(".page__hero-typewriter");
  if (!target || !source) return;

  const text = source.getAttribute("aria-label") || "";
  let i = 0;

  function type() {
    if (i < text.length) {
      target.textContent += text.charAt(i);
      i += 1;
      setTimeout(type, 45);
    }
  }

  type();
})();
(function () {
  if (!window.matchMedia || window.matchMedia("(hover: none), (pointer: coarse), (prefers-reduced-motion: reduce)").matches) {
    return;
  }

  const orbit = document.createElement("div");
  orbit.className = "cursor-orbit";
  document.body.appendChild(orbit);

  let targetX = window.innerWidth / 2;
  let targetY = window.innerHeight / 2;
  let currentX = targetX;
  let currentY = targetY;
  let visible = false;

  document.addEventListener("mousemove", function (event) {
    targetX = event.clientX;
    targetY = event.clientY;
    if (!visible) {
      visible = true;
      orbit.style.opacity = "1";
    }
  });

  document.addEventListener("mouseleave", function () {
    visible = false;
    orbit.style.opacity = "0";
  });

  document.addEventListener("click", function (event) {
    const ripple = document.createElement("span");
    ripple.className = "cursor-ripple";
    ripple.style.left = event.clientX + "px";
    ripple.style.top = event.clientY + "px";
    document.body.appendChild(ripple);
    ripple.addEventListener("animationend", function () {
      ripple.remove();
    });
  });

  function animate() {
    currentX += (targetX - currentX) * 0.12;
    currentY += (targetY - currentY) * 0.12;
    orbit.style.transform = "translate3d(" + currentX + "px, " + currentY + "px, 0) translate(-50%, -50%)";
    requestAnimationFrame(animate);
  }

  animate();
})();
</script>

<h1 id="about">About me</h1>

<p>I am an incoming <strong>Ph.D. student in Electrical and Computer Engineering</strong> at <a href="https://engineering.purdue.edu/ECE">Purdue University</a>, advised by Prof. <a href="https://ziranw.github.io/">Ziran Wang</a>. Before that, I received my M.S. in Computer Science from <a href="https://www.columbia.edu/">Columbia University</a> and my B.Eng. from <a href="https://www.zju.edu.cn/english/">Zhejiang University</a>.</p>

<p>My research interests broadly lie in <span class="research-keyword">machine learning</span> and its intersections with <span class="research-keyword">autonomous systems</span> and <span class="research-keyword">computer vision</span>. I am especially interested in building <span class="research-keyword">interpretable</span> and <span class="research-keyword">generalizable learning-based systems</span> that support effective, robust, safe, and trustworthy autonomy.</p>

<p>I’m always happy to chat about research, collaborations, or shared interests — feel free to reach out via email! 🤝✨</p>

<h1 id="news">News</h1>

<p><strong>[Aug 2026]</strong> I am excited to begin my Ph.D. journey at Purdue ECE. Boiler Up! 🚂🎓🌟</p>
<p><strong>[Jan 2026]</strong> Our <a href="https://arxiv.org/abs/2603.04329">paper</a> on uncertainty-aware robot navigation was accepted to ACC 2026 🎉</p>

<h1 id="projects">Projects</h1>

{% for post in site.projects reversed %}
  {% include archive-single.html %}
{% endfor %}

<h1 id="teaching">Teaching</h1>

<p>COMS 4995 – Deep Learning for Computer Vision, TA, Fall 2025, Columbia University</p>