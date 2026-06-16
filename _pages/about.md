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
  min-height: 420px;
  margin: -2rem calc(50% - 50vw) 2rem 0;
  padding: 2rem;
  display: flex;
  align-items: flex-end;
  overflow: hidden;
  border-radius: 0;
  background-image:
    linear-gradient(90deg, rgba(0,0,0,0.72) 0%, rgba(0,0,0,0.50) 42%, rgba(0,0,0,0.08) 72%, rgba(0,0,0,0) 100%),
    url('/images/landscape.png');
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

@media (max-width: 600px) {
  .about-hero {
    min-height: 420px;
    padding: 1.25rem;
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

</style>

<script>
(function () {
  const text = "robot_learning / safe_autonomy / uncertainty_aware_navigation";
  const target = document.getElementById("typed-text");
  if (!target) return;

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
</script>


<!-- This is the front page of a website that is powered by the [academicpages template](https://github.com/academicpages/academicpages.github.io) and hosted on GitHub pages.  -->

<h1 id="news">News</h1>

**[Aug 2026]** I am excited to begin my Ph.D. journey at Purdue ECE. Boiler Up! 🚂🎓🌟  
**[Jan 2026]** Our [paper](https://arxiv.org/abs/2603.04329) on uncertainty-aware robot navigation was accepted to ACC 2026 🎉



<h1 id="projects">Projects</h1>

{% for post in site.projects reversed %}
  {% include archive-single.html %}
{% endfor %}


<h1 id="teaching">Teaching</h1>

<p>COMS 4995 – Deep Learning for Computer Vision, TA, Fall 2025, Columbia University</p>
