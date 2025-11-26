---
layout: default
title: "Gallery Home"
---

<h2>Artwork</h2>
<div class="gallery-grid">
  {% for art in site.data.artwork %}
    <div class="gallery-item">
      <a href="{{ art.url | relative_url }}">
        <img src="{{ art.thumbnail | relative_url }}" alt="{{ art.title }}">
      </a>
      <p>{{ art.title }}</p>
    </div>
  {% endfor %}
</div>

<style>
.gallery-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
  justify-content: center;
}
.gallery-item img {
  width: 200px;
  border-radius: 4px;
  transition: transform 0.2s ease;
}
.gallery-item img:hover {
  transform: scale(1.05);
}
</style>
