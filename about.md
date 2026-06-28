---
layout: default
title: About Us
permalink: /about/
---

![GroupPhotoSYVB](https://live.staticflickr.com/65535/55111940598_7d651d9422_c.jpg)

We are the Singapore Youth Voices for Biodiversity. We are run by youths, for youths.

## Our Mission

- We aim to raise awareness about Singapore's biodiversity, while carrying out conservation through making changes in our national biodiversity policies.
- We analyse policies that involve or affect biodiversity, like land-use planning, and seek to **balance** development with conservation.
- The ideal world is one where we don't need to exist, because efficient development is carried out with conservation of sensitive biodiversity already in mind. 

# Meet Our Core Team

{% assign sorted_people = site.people | sort: "order" %}

<div class="people-grid">
  {% for person in sorted_people %}
  <a href="{{ person.url }}" style="text-decoration: none; color: inherit;">
  <div class="person-card">
    {% if person.coverimg %}
    <div class="person-cover">
      <img src="{{ person.coverimg }}" alt="{{ person.title }}" loading="lazy">
    </div>
    {% endif %}
    
    <div class="person-content">
      <h3 class="person-title">{{ person.title }}</h3>
      <p class="person-role">{{ person.role }}</p>
      
      {% if person.content %}
      <p class="person-bio">
        {{ person.content | strip_html | truncatewords: 30 }}
      </p>
      {% endif %}
    </div>
  </div>
  </a>
  {% endfor %}
</div>

<style>
.people-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
  margin: 2rem 0;
}

@media (min-width: 768px) {
  .people-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

.person-card {
  border: 1px solid #e0e0e0;
  border-radius: 8px;
  overflow: hidden;
  box-shadow: 0 2px 8px rgba(0,0,0,0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

@media (prefers-color-scheme: dark) {
  .person-card {
    border-color: #444;
    box-shadow: 0 2px 8px rgba(0,0,0,0.5);
  }
}

.person-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 4px 12px rgba(0,0,0,0.15);
}

@media (prefers-color-scheme: dark) {
  .person-card:hover {
    box-shadow: 0 4px 12px rgba(0,0,0,0.7);
  }
}

.person-cover {
  width: 100%;
  height: 200px;
  overflow: hidden;
  background-color: #f0f0f0;
}

@media (prefers-color-scheme: dark) {
  .person-cover {
    background-color: #2a2a2a;
  }
}

.person-cover img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.person-content {
  padding: 1.5rem;
}

.person-title {
  font-family: 'Lexend', sans-serif;
  font-weight: 700;
  margin: 0 0 0.5rem 0;
  font-size: 1.25rem;
  font-weight: 600;
}

.person-role {
  margin: 0 0 1rem 0;
  color: #666;
  font-style: italic;
  font-size: 0.95rem;
}

@media (prefers-color-scheme: dark) {
  .person-role {
    color: #aaa;
  }
}

.person-bio {
  margin: 0;
  color: #000;
  line-height: 1.6;
  font-size: 0.95rem;
  display: -webkit-box;
  -webkit-line-clamp: 3;
  -webkit-box-orient: vertical;
  overflow: hidden;
  text-overflow: ellipsis;
}

@media (prefers-color-scheme: dark) {
  .person-bio {
    color: #e0e0e0;
  }
}
</style>