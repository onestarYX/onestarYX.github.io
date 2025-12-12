---
permalink: /
title: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

About Me
======
Hi, I'm Yixing Wang, a 2nd year CS PhD student at the University of Michigan, advised by Prof. [Stella Yu](https://web.eecs.umich.edu/~stellayu/). I'm broadly insterested in 2D/3D computer vision and robotics with current research focused on unsupervised visual representation learning and 3D scene understanding.

Previously, I obtained a M.S. degree in Computer Science at Stanford University, where I had the privillage of working closely with Prof. [Jiajun Wu](https://jiajunwu.com/). Before that, I earned a B.S. degree in Computer Scicence from UC San Diego.

<span class="text-red">I'm actively seeking internship opportunities for summer 2026. Please feel free to reach out if you’d like to chat or explore potential collaborations!</span>


Selected Publications
======
{% assign pubs = site.publications | sort: "date" | reverse %}
{% assign selected_true = pubs | where: "selected", true %}
{% assign featured_true = pubs | where: "featured", true %}
{% assign selected_pubs = selected_true | concat: featured_true | uniq %}

{% if selected_pubs and selected_pubs.size > 0 %}
  {% assign pubs_to_show = selected_pubs %}
{% else %}
  {% assign pubs_to_show = pubs | slice: 0, 5 %}
{% endif %}

{% for post in pubs_to_show %}
  {% include archive-single.html %}
{% endfor %}

[See all publications]({{ "/publications/" | relative_url }})

Teaching
======
- Graduate Student Instructor, EECS 542—Advanced Topics in Computer Vision, UMich	
- Tutor, CSE 151A—Introduction to Machine Learning, UC San Diego


Professonal Services
======
- Reviewer for ICCV'23, 25.