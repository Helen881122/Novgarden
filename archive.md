---
layout: default  
title: 藏经阁
---

# 外部链接存档

<div class="archive-grid">
  <div class="archive-item brick-border">
    <div class="platform-icon">📱</div>
    <h3>微博作品集</h3>
    <p>最新的剧场摄影作品更新</p>
    <div class="archive-actions">
      <button class="preview-btn" onclick="openPreview('https://weibo.com')">预览</button>
      <a href="https://weibo.com" target="_blank" class="visit-btn">访问原链接</a>
    </div>
  </div>
  
  <div class="archive-item brick-border">
    <div class="platform-icon">🎬</div>
    <h3>B站视频</h3>
    <p>幕后花絮和创作过程</p>
    <div class="archive-actions">
      <button class="preview-btn" onclick="openPreview('https://bilibili.com')">预览</button>
      <a href="https://bilibili.com" target="_blank" class="visit-btn">访问原链接</a>
    </div>
  </div>
</div>

<!-- 预览模态框 -->
<div id="previewModal" class="modal">
  <div class="modal-content">
    <span class="close" onclick="closePreview()">&times;</span>
    <iframe id="previewFrame" src=""></iframe>
  </div>
</div>

<style>
.archive-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 1.5rem;
}

.archive-item {
  padding: 1.5rem;
  text-align: center;
}

.platform-icon {
  font-size: 2rem;
  margin-bottom: 1rem;
}

.archive-actions {
  display: flex;
  gap: 0.5rem;
  margin-top: 1rem;
}

.preview-btn, .visit-btn {
  flex: 1;
  padding: 0.5rem;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  text-decoration: none;
  font-size: 0.9rem;
}

.preview-btn {
  background: #B54F42;
  color: white;
}

.visit-btn {
  background: #F5F1E6;
  color: #333;
  border: 1px solid #8C8C8C;
}

/* 模态框样式 */
.modal {
  display: none;
  position: fixed;
  z-index: 2000;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0,0,0,0.8);
}

.modal-content {
  position: relative;
  background-color: #fefefe;
  margin: 5% auto;
  padding: 20px;
  border: 1px solid #888;
  width: 90%;
  height: 80%;
  border-radius: 8px;
}

.close {
  color: #aaa;
  float: right;
  font-size: 28px;
  font-weight: bold;
  cursor: pointer;
}

.close:hover {
  color: black;
}

#previewFrame {
  width: 100%;
  height: calc(100% - 40px);
  border: none;
  margin-top: 10px;
}
</style>

<script>
function openPreview(url) {
  document.getElementById('previewFrame').src = url;
  document.getElementById('previewModal').style.display = 'block';
}

function closePreview() {
  document.getElementById('previewModal').style.display = 'none';
  document.getElementById('previewFrame').src = '';
}
</script>
