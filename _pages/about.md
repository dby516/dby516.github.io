---
permalink: /
# title: "academicpages is a ready-to-fork GitHub Pages template for academic personal websites"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---
<!-- 
<h1 id="about">About me</h1>

I am an incoming Ph.D. student in Electrical and Computer Engineering at [Purdue University](https://engineering.purdue.edu/ECE), advised by Prof. [Ziran Wang](https://ziranw.github.io/). Before that, I received my M.S. in Computer Science from [Columbia University](https://www.columbia.edu/) and my B.Eng. from [Zhejiang University](https://www.zju.edu.cn/english/).  

My research interests lie broadly in Machine Learning, Deep Learning and their intersections with Robot Navigation, Manipulation and Computer Vision. I'm especially interested in enabling learning-based methods to benefit robot navigation and motion in open-world environments, as well as in quantifying and constraining the uncertainty introduced by learning methods to form a strong, effective, safe, and trustworthy autonomous system.  

I’m always happy to chat about research, collaborations, or shared interests — feel free to reach out via email! 🤝✨ -->

<section class="about-hero">

  <div class="about-hero__grid"></div>
  <div class="about-hero__glow"></div>

  <div class="about-hero__content hero-text">
    <div class="typewriter">
      <span id="typed-text"></span><span class="cursor">|</span>
    </div>
    <h1 id="about">About me</h1>
    <p>I am an incoming Ph.D. student in Electrical and Computer Engineering at <a href="https://engineering.purdue.edu/ECE">Purdue University</a>, advised by Prof. <a href="https://ziranw.github.io/">Ziran Wang</a>. Before that, I received my M.S. in Computer Science from <a href="https://www.columbia.edu/">Columbia University</a> and my B.Eng. from <a href="https://www.zju.edu.cn/english/">Zhejiang University</a>.</p>
    <p>My research interests lie broadly in Machine Learning, Deep Learning and their intersections with Robot Navigation, Manipulation and Computer Vision. I'm especially interested in enabling learning-based methods to benefit robot navigation and motion in open-world environments, as well as in quantifying and constraining the uncertainty introduced by learning methods to form a strong, effective, safe, and trustworthy autonomous system.</p>
    <p>I’m always happy to chat about research, collaborations, or shared interests — feel free to reach out via email! 🤝✨</p>
  </div>
</section>

<style>
.page__content {
  padding-top: 0;
  margin-top: 0;
}

.about-hero {
  position: relative;
  min-height: calc(100vh - 72px);
  margin: -2rem -2rem 0 0;
  padding: 2rem;
  display: flex;
  align-items: center;
  overflow: hidden;
  border-radius: 0;
  background-image:
    linear-gradient(90deg, rgba(0,0,0,0.72) 0%, rgba(0,0,0,0.50) 42%, rgba(0,0,0,0.08) 72%, rgba(0,0,0,0) 100%),
    url('/images/landscape.jpg');
  background-size: cover;
  background-position: center;
}
.about-hero__content {
  position: relative;
  z-index: 2;
  max-width: 780px;
  color: #fff;
  text-shadow: 0 2px 14px rgba(0, 0, 0, 0.45);
}

.about-hero__grid {
  position: absolute;
  inset: 0;
  z-index: 1;
  opacity: 0.16;
  background-image:
    linear-gradient(rgba(158,231,255,0.18) 1px, transparent 1px),
    linear-gradient(90deg, rgba(158,231,255,0.18) 1px, transparent 1px);
  background-size: 36px 36px;
  -webkit-mask-image: linear-gradient(90deg, #000 0%, #000 38%, transparent 72%);
  mask-image: linear-gradient(90deg, #000 0%, #000 38%, transparent 72%);
  animation: gridDrift 18s linear infinite;
}

.typewriter {
  margin-bottom: 14px;
  font-family: "SFMono-Regular", "Consolas", monospace;
  color: #9ee7ff;
  font-size: 0.95rem;
  letter-spacing: 0.03em;
}

.cursor {
  animation: blink 1s infinite;
}

.hero-text p {
  opacity: 0;
  transform: translateY(10px);
  animation: fadeUp 0.7s ease forwards;
}

.hero-text p:nth-of-type(1) { animation-delay: 0.2s; }
.hero-text p:nth-of-type(2) { animation-delay: 0.4s; }
.hero-text p:nth-of-type(3) { animation-delay: 0.6s; }

@keyframes blink {
  0%, 50% { opacity: 1; }
  51%, 100% { opacity: 0; }
}

@keyframes fadeUp {
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes gridDrift {
  from { background-position: 0 0; }
  to { background-position: 72px 36px; }
}

.about-hero h1 {
  margin-top: 0;
  color: #fff;
}

.about-hero p {
  color: #fff;
}

.about-hero a {
  color: #fff;
  text-decoration: underline;
}

.about-hero__glow {
  position: absolute;
  left: 50%;
  top: 50%;
  width: 240px;
  height: 240px;
  border-radius: 50%;
  pointer-events: none;
  z-index: 1;
  opacity: 0;
  background: radial-gradient(circle, rgba(56,189,248,0.22), transparent 66%);
  transform: translate(-50%, -50%);
  transition: opacity 0.2s ease;
  mix-blend-mode: screen;
}

.about-hero:hover .about-hero__glow {
  opacity: 1;
}


@media (max-width: 600px) {
  .about-hero {
    min-height: 420px;
    padding: 1.25rem;
  }
  .about-hero__glow {
    display: none;
  }
}


#news,
#projects,
#teaching {
  margin-top: 3.5rem;
}

#news {
  margin-top: 2.5rem;
}

#projects,
#teaching {
  padding-top: 1rem;
}

.home-reveal {
  position: relative;
  z-index: 4;
  margin: -54px -2rem 0 0;
  padding: 54px 2rem 0 2rem;
  background: #fff;
  border-top: 1px solid rgba(15, 23, 42, 0.08);
  box-shadow: 0 -18px 40px rgba(15, 23, 42, 0.08);
}

.home-reveal__handle {
  position: absolute;
  top: 16px;
  left: 50%;
  width: 72px;
  height: 5px;
  border-radius: 999px;
  background: rgba(15, 23, 42, 0.22);
  transform: translateX(-50%);
}

</style>

<script>
(function () {
  const text = "robot_learning / safe_autonomy / uncertainty_aware_navigation";
  const target = document.getElementById("typed-text");

  if (target) {
    let i = 0;
    function type() {
      if (i < text.length) {
        target.textContent += text.charAt(i);
        i += 1;
        setTimeout(type, 45);
      }
    }
    type();
  }

  const hero = document.querySelector(".about-hero");
  const glow = document.querySelector(".about-hero__glow");

  if (hero && glow) {
    hero.addEventListener("mousemove", function (event) {
      const rect = hero.getBoundingClientRect();
      glow.style.left = event.clientX - rect.left + "px";
      glow.style.top = event.clientY - rect.top + "px";
    });
  }
})();
</script>


<!-- This is the front page of a website that is powered by the [academicpages template](https://github.com/academicpages/academicpages.github.io) and hosted on GitHub pages.  -->


<section class="home-reveal">
  <div class="home-reveal__handle"></div>

  <h1 id="news">News</h1>

  <p><strong>[Aug 2026]</strong> I am excited to begin my Ph.D. journey at Purdue ECE. Boiler Up! 🚂🎓🌟</p>
  <p><strong>[Jan 2026]</strong> Our <a href="https://arxiv.org/abs/2603.04329">paper</a> on uncertainty-aware robot navigation was accepted to ACC 2026 🎉</p>

  <h1 id="projects">Projects</h1>

  {% for post in site.projects reversed %}
    {% include archive-single.html %}
  {% endfor %}

  <h1 id="teaching">Teaching</h1>

  <p>COMS 4995 – Deep Learning for Computer Vision, TA, Fall 2025, Columbia University</p>
</section>