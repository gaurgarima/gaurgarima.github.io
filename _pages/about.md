---
permalink: /
redirect_from:
  - /about/
  - /about.html
---

{% include base_path %}

<section class="home-intro">
  <p>
    My research focuses on AI for data management, particularly knowledge graphs, data provenance, and fact-checking for investigative journalism.
  </p>
  <p>
    Previously, I was a postdoctoral researcher at Inria Saclay and IIT Delhi. I received my PhD in Computer Science from IIT Kanpur.
  </p>
</section>

<section class="home-section">
  <h2>Teaching</h2>
  <ul class="home-teaching">
    {% assign teaching_sorted = site.teaching | sort: "date" | reverse %}
    {% for item in teaching_sorted limit:2 %}
      <li>
        <a href="{{ item.url }}">{{ item.title }}</a>
        <span class="home-meta">{{ item.venue }}, {{ item.date | date: "%Y" }}</span>
      </li>
    {% endfor %}
  </ul>
  <p><a href="/teaching/">Teaching experience</a></p>
</section>

<section class="home-section">
  <h2>Selected publications</h2>
  <ul class="home-publications">
    {% assign publications_sorted = site.publications | sort: "date" | reverse %}
    {% for pub in publications_sorted limit:3 %}
      <li>
        <a href="{{ pub.url }}">{{ pub.title }}</a>
        <span class="home-meta">{% if pub.venue %}{{ pub.venue }}{% else %}{{ pub.date | date: "%Y" }}{% endif %}</span>
      </li>
    {% endfor %}
  </ul>
  <p><a href="/publications/">All publications</a></p>
</section>
