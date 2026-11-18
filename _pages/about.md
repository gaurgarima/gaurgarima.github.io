---
permalink: /
title: "About me"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

<style>
.home-section {
  margin-bottom: 2.25rem;
}
.home-section h2 {
  margin-top: 0;
}
.home-lead {
  font-size: 1.05rem;
  line-height: 1.65;
}
.home-chip-list {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
  margin: 0.75rem 0 0;
  padding: 0;
  list-style: none;
}
.home-chip-list li {
  padding: 0.25rem 0.6rem;
  border: 1px solid var(--global-border-color);
  border-radius: 999px;
  font-size: 0.85rem;
}
.home-list {
  margin-left: 0;
  padding-left: 0;
  list-style: none;
}
.home-list li {
  margin-bottom: 0.95rem;
}
.home-meta {
  display: block;
  margin-top: 0.15rem;
  color: var(--global-text-color-light);
  font-size: 0.9rem;
}
.home-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 0.75rem;
  margin-top: 1rem;
}
.home-actions a {
  text-decoration: none;
}
</style>

<section class="home-section">
  <p class="home-lead">
    I am a postdoctoral researcher in the CEDAR team at Inria Saclay, working with Ioana Manolescu.
    My research is in AI for data management, with applications in investigative journalism and fact-checking.
    I work on knowledge graphs, provenance, data integration, information extraction, and named-entity-centric data management.
  </p>
  <p>
    Before joining Inria in February 2024, I was a postdoctoral researcher and research scientist at IIT Delhi with Maya Ramanath.
    I completed my PhD at IIT Kanpur under Arnab Bhattacharya and Srikanta Bedathur.
  </p>
  <div class="home-actions">
    <a class="btn" href="/publications/">Publications</a>
    <a class="btn" href="/teaching/">Teaching</a>
    <a class="btn" href="/cv/">CV</a>
  </div>
</section>

<section class="home-section">
  <h2>Interests</h2>
  <ul class="home-chip-list">
    <li>Graph data management</li>
    <li>Provenance</li>
    <li>Knowledge graphs</li>
    <li>Data integration</li>
    <li>Fact-check retrieval</li>
    <li>Information extraction</li>
    <li>Named entity cleaning</li>
  </ul>
</section>

<section class="home-section">
  <h2>Teaching</h2>
  <p>
    I teach and support courses in database systems, big graph databases, and big data systems at Ecole Polytechnique, Telecom Paris, and IIT Kanpur/NPTEL.
  </p>
  <ul class="home-list">
    {% assign teaching_sorted = site.teaching | sort: "date" | reverse %}
    {% for item in teaching_sorted limit:3 %}
      <li>
        <a href="{{ item.url }}">{{ item.title }}</a>
        <span class="home-meta">{{ item.type }}, {{ item.venue }}, {{ item.date | date: "%Y" }}</span>
      </li>
    {% endfor %}
  </ul>
  <p><a href="/teaching/">See all teaching</a></p>
</section>

<section class="home-section">
  <h2>Featured Publications</h2>
  <ul class="home-list">
    {% assign publications_sorted = site.publications | sort: "date" | reverse %}
    {% for pub in publications_sorted limit:3 %}
      <li>
        <a href="{{ pub.url }}">{{ pub.title }}</a>
        <span class="home-meta">{{ pub.venue }}, {{ pub.date | date: "%Y" }}</span>
        {% if pub.paperurl %}
          <span class="home-meta"><a href="{{ pub.paperurl }}">Paper</a>{% if pub.codeurl %} | <a href="{{ pub.codeurl }}">Code</a>{% endif %}{% if pub.toolurl %} | <a href="{{ pub.toolurl }}">Tool</a>{% endif %}{% if pub.dataseturl %} | <a href="{{ pub.dataseturl }}">Dataset</a>{% endif %}</span>
        {% endif %}
      </li>
    {% endfor %}
  </ul>
</section>

<section class="home-section">
  <h2>Education</h2>
  <ul class="home-list">
    <li>
      PhD (with MTech), Computer Science and Engineering
      <span class="home-meta">IIT Kanpur, 2021</span>
    </li>
    <li>
      BE, Information Technology
      <span class="home-meta">Madhav Institute of Technology and Science, Gwalior, 2013</span>
    </li>
  </ul>
</section>
