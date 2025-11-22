---
layout: default
title: 首页
---

# 欢迎来到剧场园林

<div class="spotlight-container">
  <div class="brick-border">
    <h2>最新作品</h2>
    <p>探索剧场摄影的独特魅力</p>
  </div>
</div>

<script>
// 聚光灯效果
document.addEventListener('mousemove', function(e) {
  const overlay = document.querySelector('.spotlight-overlay');
  if (overlay) {
    overlay.style.setProperty('--mouse-x', e.clientX + 'px');
    overlay.style.setProperty('--mouse-y', e.clientY + 'px');
  }
});
</script>
