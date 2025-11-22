---
layout: default
title: 画廊
---

# 摄影作品

<div class="gallery-grid">
  <div class="gallery-item brick-border">
    <img src="/assets/images/placeholder1.jpg" alt="作品1">
    <h3>作品标题</h3>
    <p>作品描述</p>
  </div>
  
  <div class="gallery-item brick-border">
    <img src="/assets/images/placeholder2.jpg" alt="作品2">
    <h3>作品标题</h3>
    <p>作品描述</p>
  </div>
</div>

<style>
.gallery-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
  margin: 2rem 0;
}

.gallery-item {
  padding: 1rem;
  transition: transform 0.3s ease;
}

.gallery-item:hover {
  transform: translateY(-5px);
}

.gallery-item img {
  width: 100%;
  height: 200px;
  object-fit: cover;
  border: 1px solid #8C8C8C;
}
</style>
