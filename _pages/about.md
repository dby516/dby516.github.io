---
permalink: /
# title: "academicpages is a ready-to-fork GitHub Pages template for academic personal websites"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<h1 id="about">About me</h1>

I am an incoming Ph.D. student in Electrical and Computer Engineering at [Purdue University](https://engineering.purdue.edu/ECE), advised by Prof. [Ziran Wang](https://ziranw.github.io/). Before that, I received my M.S. in Computer Science from [Columbia University](https://www.columbia.edu/) and my B.Eng. from [Zhejiang University](https://www.zju.edu.cn/english/).  

My research interests lie broadly in Machine Learning, Deep Learning and their intersections with Robot Navigation, Manipulation and Computer Vision. I'm especially interested in enabling learning-based methods to benefit robot navigation and motion in open-world environments, as well as in quantifying and constraining the uncertainty introduced by learning methods to form a strong, effective, safe, and trustworthy autonomous system.  

I’m always happy to chat about research, collaborations, or shared interests — feel free to reach out via email! 🤝✨


<!-- This is the front page of a website that is powered by the [academicpages template](https://github.com/academicpages/academicpages.github.io) and hosted on GitHub pages.  -->

News
======
**[Aug 2026]** I am excited to begin my Ph.D. journey at Purdue ECE. Boiler Up! 🚂🎓🌟  
**[Jan 2026]** Our paper on uncertainty-aware robot navigation was accepted to ACC 2025 🎉



<h1 id="projects">Projects</h1>

{% for post in site.projects reversed %}
  {% include archive-single.html %}
{% endfor %}


<h1 id="teaching">Teaching</h1>

<p>COMS 4995 – Deep Learning for Computer Vision, TA, Fall 2025, Columbia University</p>
