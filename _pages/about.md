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

<section class="about-hero" style="background-image: linear-gradient(90deg, rgba(0,0,0,0.68) 0%, rgba(0,0,0,0.48) 42%, rgba(0,0,0,0.10) 72%, rgba(0,0,0,0) 100%), url('/images/landscape.jpg');">
  <div class="about-hero__content">
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
  min-height: 420px;
  margin: -2rem calc(50% - 50vw) 2rem 0;
  padding: 2rem;
  display: flex;
  align-items: flex-end;
  background-size: cover;
  background-position: center;
  border-radius: 0;
}

.about-hero__content {
  max-width: 760px;
  color: #fff;
  text-shadow: 0 2px 14px rgba(0, 0, 0, 0.45);
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
