---
layout: page
title: Projects
---

I've worked on a wide range of interesting projects during my career. Aerospace engineering, my academic background, is highly multidisciplinary, so I have broad knowledge in engineering that supports my depth in high performance computing for various applications. Since I finished my PhD in 2012, the common thread to my work has been integrating vision-based systems for contexts including surveillance, remote sensing, and autonomous vehicle perception.

Here's a sampling of some of the things I've worked on:

<div class="ui container">
  <div class="ui stackable centered three cards">
    {% for project in site.projects reversed %}
      <a class="card" href="{{ project.url | prepend: site.baseurl }}">
        <div class="project_card_image">
            <img class="ui middle aligned image" alt="{{ project.title }}" src="{{ project.image | prepend: site.baseurl }}">
        </div>
        <div class="content">
          <span class="header">{{ project.title }}</span>
          <div class="description">{{ project.summary }}</div>
        </div>
        <div class="ui bottom attached button">Read More</div>
      </a>
    {% endfor %}
  </div>
</div>