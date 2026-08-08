---
permalink: /
title: "Nghia Nguyen-Trung"
excerpt: "Ph.D. Candidate in Statistics and Operations Research at UNC Chapel Hill"
author_profile: true
header:
  og_image: "/images/Nghia.png"
redirect_from: 
  - /about/
  - /about.html
---

I am a Ph.D. Candidate in the [Department of Statistics and Operations Research](https://stor.unc.edu/) at the [University of North Carolina at Chapel Hill](https://unc.edu/), advised by [Prof. Quoc Tran-Dinh](https://quoctd.web.unc.edu/). My expected graduation date is **May 2027**.

### Research Interests
My research lies in mathematical optimization, numerical algorithms, and continuous operator theory, with a focus on:
* **First-Order Methods under Nonmonotonicity:** Extragradient and its generalizations, operator splitting methods, Halpern and Krasnosel'skiǐ-Mann-type iterations, etc.
* **Deterministic & Stochastic Methods:** Scalable optimization schemes spanning classical deterministic frameworks to modern stochastic regimes, leveraging mini-batching, variance reduction, and block-coordinate techniques for large-scale problems.
* **Distributed Computing:** Asynchronous, parallel, and decentralized consensus frameworks designed for large-scale optimization over complex network architectures.

### Education & Background
* **Ph.D. & M.S. in Statistics and Operations Research**, UNC Chapel Hill (M.S. earned in 2025).
* **Engineer in Mathematics and Informatics**, [Hanoi University of Science and Technology](https://hust.edu.vn/) (2022). 
  * *Honors:* **Valedictorian of the Class of 2022 (Ranked 1st)**; advised by [Prof. Nguyen Thi Thu Thuy](https://sami.hust.edu.vn/hoc-tap/giang-vien/?name=thuyntt).

<style>
.badge-new {
  background-color: #e74c3c;
  color: #ffffff;
  font-size: 0.7em;
  font-weight: bold;
  padding: 2px 7px;
  border-radius: 10px;
  margin-left: 6px;
  display: inline-block;
  vertical-align: middle;
  box-shadow: 0 0 4px rgba(231, 76, 60, 0.6);
  animation: blinker 1.2s linear infinite;
}

@keyframes blinker {
  50% { opacity: 0.25; }
}

.news-list {
  margin-top: 12px;
  margin-bottom: 10px;
  padding-left: 20px;
}

.news-list li {
  margin-bottom: 10px;
  line-height: 1.5;
}
</style>

### Recent News

<ul class="news-list">
  {% assign sorted_news = site.news | sort: "date" | reverse %}
  {% for item in sorted_news limit: 4 %}
    <li>
      <b>[{{ item.date_display }}]</b> {{ item.content | markdownify | remove: '<p>' | remove: '</p>' }}
      {% if item.is_new %}
        <span class="badge-new">NEW</span>
      {% endif %}
    </li>
  {% endfor %}
</ul>

<p style="text-align: right; margin-bottom: 25px;">
  <a href="/talks/" style="font-style: italic;">See all news &amp; talks &rarr;</a>
</p>

### Contact
**Nghia Nguyen-Trung, M.S.**<br />
_Department of Statistics and Operations Research_<br />
Address: B48 Hanes Hall, University of North Carolina at Chapel Hill, Chapel Hill, NC 27516, USA<br />
Email: [nghiant@unc.edu](mailto:nghiant@unc.edu)<br />
My name in native language: **Nguyễn Trung Nghĩa** _(**Nghĩa** is my first name)_
