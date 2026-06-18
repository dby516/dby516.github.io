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
.cursor-mesh {
  position: fixed;
  inset: 0;
  width: 100vw;
  height: 100vh;
  pointer-events: none;
  z-index: 9999;
}

@media (hover: none), (pointer: coarse), (prefers-reduced-motion: reduce) {
  .cursor-mesh {
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

  const canvas = document.createElement("canvas");
  canvas.className = "cursor-mesh";
  canvas.setAttribute("aria-hidden", "true");
  document.body.appendChild(canvas);

  const ctx = canvas.getContext("2d");
  const pointCount = 7;
  const nodes = [];
  let dpr = 1;
  let width = 0;
  let height = 0;
  let mouseX = window.innerWidth / 2;
  let mouseY = window.innerHeight / 2;
  let centerX = mouseX;
  let centerY = mouseY;
  let visible = false;
  let impulse = 0;

  for (let index = 0; index < pointCount; index += 1) {
    nodes.push({
      x: mouseX,
      y: mouseY,
      vx: 0,
      vy: 0,
      angle: (Math.PI * 2 * index) / pointCount,
      radius: 28 + (index % 3) * 13
    });
  }

  function resize() {
    dpr = Math.min(window.devicePixelRatio || 1, 2);
    width = window.innerWidth;
    height = window.innerHeight;
    canvas.width = Math.round(width * dpr);
    canvas.height = Math.round(height * dpr);
    canvas.style.width = width + "px";
    canvas.style.height = height + "px";
    ctx.setTransform(dpr, 0, 0, dpr, 0, 0);
  }

  function drawLine(a, b, alpha) {
    ctx.strokeStyle = "rgba(14, 165, 233, " + alpha + ")";
    ctx.lineWidth = 1;
    ctx.beginPath();
    ctx.moveTo(a.x, a.y);
    ctx.lineTo(b.x, b.y);
    ctx.stroke();
  }

  function animate() {
    ctx.clearRect(0, 0, width, height);

    centerX += (mouseX - centerX) * 0.14;
    centerY += (mouseY - centerY) * 0.14;
    impulse *= 0.9;

    if (visible) {
      const time = performance.now() * 0.001;
      const center = { x: centerX, y: centerY };
      const baseAlpha = 0.18 + impulse * 0.08;
      const webRadius = 1 + impulse * 0.65;

      nodes.forEach(function (node, index) {
        const drift = time * (0.7 + index * 0.08);
        const targetRadius = (node.radius + Math.sin(time * 1.3 + index) * 7) * webRadius;
        const targetAngle = node.angle + drift;
        const targetX = centerX + Math.cos(targetAngle) * targetRadius;
        const targetY = centerY + Math.sin(targetAngle) * targetRadius;

        node.vx += (targetX - node.x) * 0.045;
        node.vy += (targetY - node.y) * 0.045;
        node.vx *= 0.72;
        node.vy *= 0.72;
        node.x += node.vx;
        node.y += node.vy;
      });

      nodes.forEach(function (node) {
        const distance = Math.hypot(node.x - centerX, node.y - centerY);
        const alpha = Math.max(0, baseAlpha - distance / 420);
        drawLine(center, node, alpha);
      });

      for (let a = 0; a < nodes.length; a += 1) {
        for (let b = a + 1; b < nodes.length; b += 1) {
          const distance = Math.hypot(nodes[a].x - nodes[b].x, nodes[a].y - nodes[b].y);
          if (distance < 95) {
            drawLine(nodes[a], nodes[b], (1 - distance / 95) * (0.28 + impulse * 0.12));
          }
        }
      }

      nodes.forEach(function (node) {
        ctx.fillStyle = "rgba(14, 165, 233, 0.42)";
        ctx.beginPath();
        ctx.arc(node.x, node.y, 2.1 + impulse * 0.6, 0, Math.PI * 2);
        ctx.fill();
      });

      ctx.fillStyle = "rgba(14, 165, 233, 0.22)";
      ctx.beginPath();
      ctx.arc(centerX, centerY, 1.8 + impulse * 0.4, 0, Math.PI * 2);
      ctx.fill();
    }

    requestAnimationFrame(animate);
  }

  document.addEventListener("mousemove", function (event) {
    mouseX = event.clientX;
    mouseY = event.clientY;
    visible = true;
  });

  document.addEventListener("mouseleave", function () {
    visible = false;
  });

  document.addEventListener("click", function () {
    impulse = 1;
  });

  window.addEventListener("resize", resize);
  resize();
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