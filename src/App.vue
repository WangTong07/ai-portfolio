<script setup>
import { ref } from 'vue';

const projects = ref([
  {
    title: 'AI 智能报告神器',
    description: '一个能将流水账一键转化为逻辑清晰、重点突出的专业日报/周报的效率工具。',
    imageUrl: 'https://img.alicdn.com/imgextra/i3/O1CN01fL1sT31i2zT1b8h9j_!!6000000004358-0-tps-1512-928.jpg',
    tags: ['Vue 3', 'Gitee', 'TCB CLI', 'Prompt Engineering'],
    liveUrl: 'http://report-assistant.app.tcloudbase.com/',
  },
  {
    title: 'AI 爆款文案神器',
    description: '你的随身文案军师。选择风格、输入关键词，即可生成引爆社交圈的趣味文案。',
    imageUrl: 'https://img.alicdn.com/imgextra/i3/O1CN01HjGjYT1mZ7g1g7D5e_!!6000000004961-0-tps-1512-928.jpg',
    tags: ['Vue 3', 'Vercel', 'UI/UX', 'Figma'],
    liveUrl: 'https://copywriting-master-pro.vercel.app/',
  },
  {
    title: 'AI 面试模拟器',
    description: '一个可以扮演资深面试官的AI Agent，能进行多轮对话，并提供专业反馈。',
    imageUrl: 'https://img.alicdn.com/imgextra/i4/O1CN01B9vV4M1i8e2w3d6E4_!!6000000004364-0-tps-1512-928.jpg',
    tags: ['Coze', 'Agent', 'Plugins', 'Workflows'],
    liveUrl: '#',
  },
  {
    title: '本地AI知识助理',
    description: '一个能处理本地文件的私人AI。支持视频/音频转文字、PDF/图片(OCR)内容提取。',
    imageUrl: 'https://img.alicdn.com/imgextra/i1/O1CN01rYdY6b1v6y4g8q6Fp_!!6000000006123-0-tps-1512-928.jpg',
    tags: ['Vue 3', 'Transformers.js', '前端AI', 'OCR'],
    liveUrl: 'https://video-summarizer-psi.vercel.app/',
  },
  {
    title: 'AI 绘画与图像生成',
    description: '探索文生图的魔法。学习使用Midjourney和Stable Diffusion，将文字转化为视觉艺术。',
    imageUrl: 'https://img.alicdn.com/imgextra/i2/O1CN013BqB2b1s9s2f5d4g3_!!6000000005721-0-tps-1512-928.jpg',
    tags: ['Midjourney', 'Stable Diffusion', '即梦AI', 'AIGC'],
    liveUrl: '#',
  },
  {
    title: 'AI 工作流自动化',
    description: '使用Coze，将文本生成、图像生成等多个AI服务串联，打造全自动内容发布机器人。',
    imageUrl: 'https://img.alicdn.com/imgextra/i3/O1CN01M6y5rY1j1c3d4e5F6_!!6000000004488-0-tps-1512-928.jpg',
    tags: ['Coze', 'Automation', 'RAG', 'API'],
    liveUrl: '#',
  },
  {
    title: 'AI Agent 框架初探',
    description: '使用Python和LangChain，构建一个能调用外部工具（搜索引擎、天气API）的智能代理。',
    imageUrl: 'https://img.alicdn.com/imgextra/i2/O1CN01C8q8qQ1r6t3c4e5F6_!!6000000005581-0-tps-1512-928.jpg',
    tags: ['Python', 'LangChain', 'Agent', 'Tools'],
    liveUrl: '#',
  },
]);
</script>

<template>
  <div class="page-wrapper">
    <div class="background-gradient"></div>
    
    <header class="hero-section">
      <div class="avatar-container">
        <img src="https://img.alicdn.com/imgextra/i1/O1CN01Lp1q1b1s9s2e5d4g2_!!6000000005721-2-tps-200-200.png" alt="Avatar" class="avatar">
        <div class="status-indicator"></div>
      </div>
      <!-- 【核心修改】将 WangTong07 替换为 疯狂的大呲花 -->
      <h1 class="main-title">你好, 我是 疯狂的大呲花</h1>
      <p class="subtitle">一个充满热情的AI学习者与创造者。在15天内，我从零开始，构建了这一系列AI应用，探索从文本生成到多模态处理的无限可能。</p>
      <div class="social-links">
        <a href="https://github.com/WangTong07" target="_blank" class="social-link">GitHub</a>
        <a href="https://gitee.com/wangtong07" target="_blank" class="social-link">Gitee</a>
      </div>
    </header>

    <main class="projects-section">
      <div class="projects-grid">
        <div class="project-card" v-for="(project, index) in projects" :key="index">
          <div class="card-image-wrapper">
            <img :src="project.imageUrl" :alt="project.title" class="card-image">
          </div>
          <div class="card-content">
            <h3 class="card-title">{{ project.title }}</h3>
            <p class="card-description">{{ project.description }}</p>
            <div class="card-tags">
              <span v-for="tag in project.tags" :key="tag" class="tag">{{ tag }}</span>
            </div>
            <div class="card-actions">
              <a :href="project.liveUrl" target="_blank" class="action-btn view-project">查看项目</a>
            </div>
          </div>
        </div>
      </div>
    </main>
  </div>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap');
:root {
  --font-sans: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Roboto', sans-serif;
  --bg-color: #030712;
  --text-color: #f9fafb;
  --text-dim-color: #9ca3af;
  --border-color: rgba(255, 255, 255, 0.1);
  --card-bg-color: #111827;
  --primary-color: #38bdf8;
}

*, *::before, *::after { box-sizing: border-box; }
body { font-family: var(--font-sans); background-color: var(--bg-color); color: var(--text-color); margin: 0; }

.page-wrapper { width: 100%; min-height: 100vh; position: relative; overflow-x: hidden; }
.background-gradient { position: absolute; top: 0; left: 0; width: 100%; height: 60vh; background: radial-gradient(ellipse 80% 50% at 50% -20%, rgba(120, 119, 198, 0.3), transparent); z-index: 0; }
.hero-section { padding: 6rem 1.5rem 4rem; text-align: center; position: relative; z-index: 1; }
.avatar-container { position: relative; display: inline-block; margin-bottom: 1.5rem; }
.avatar { width: 128px; height: 128px; border-radius: 50%; border: 4px solid rgba(255,255,255,0.1); }
.status-indicator { position: absolute; bottom: 8px; right: 8px; width: 24px; height: 24px; background-color: #22c55e; border-radius: 50%; border: 3px solid var(--bg-color); }
.main-title { font-size: 3rem; font-weight: 800; margin: 0; letter-spacing: -1.5px; }
.subtitle { max-width: 600px; margin: 1rem auto 2rem; font-size: 1.125rem; line-height: 1.8; color: var(--text-dim-color); }
.social-links { display: flex; justify-content: center; gap: 1rem; }
.social-link { padding: 0.75rem 1.5rem; border-radius: 999px; background-color: var(--card-bg-color); border: 1px solid var(--border-color); color: var(--text-color); text-decoration: none; font-weight: 500; transition: all 0.2s ease; }
.social-link:hover { background-color: var(--primary-color); border-color: var(--primary-color); color: var(--bg-color); }
.projects-section { padding: 2rem 1.5rem 6rem; position: relative; z-index: 1; }
.projects-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(320px, 1fr)); gap: 2rem; max-width: 1200px; margin: 0 auto; }
.project-card { background-color: var(--card-bg-color); border: 1px solid var(--border-color); border-radius: 16px; overflow: hidden; transition: all 0.3s ease; display: flex; flex-direction: column; }
.project-card:hover { transform: translateY(-5px); box-shadow: 0 10px 30px rgba(0,0,0,0.2); }
.card-image-wrapper { width: 100%; padding-top: 56.25%; position: relative; }
.card-image { position: absolute; top: 0; left: 0; width: 100%; height: 100%; object-fit: cover; }
.card-content { padding: 1.5rem; display: flex; flex-direction: column; flex-grow: 1; }
.card-title { font-size: 1.25rem; font-weight: 600; margin: 0 0 0.5rem; }
.card-description { font-size: 0.875rem; color: var(--text-dim-color); line-height: 1.6; flex-grow: 1; margin-bottom: 1.5rem; }
.card-tags { display: flex; flex-wrap: wrap; gap: 0.5rem; margin-bottom: 1.5rem; }
.tag { background-color: rgba(56, 189, 248, 0.1); color: var(--primary-color); padding: 0.25rem 0.75rem; border-radius: 999px; font-size: 0.75rem; font-weight: 500; }
.card-actions { margin-top: auto; padding-top: 1rem; }
.action-btn { padding: 0.75rem; border-radius: 8px; text-align: center; text-decoration: none; font-weight: 500; transition: all 0.2s ease; display: block; }
.view-project { background-color: var(--primary-color); color: var(--bg-color); }
.view-project:hover { background-color: #7dd3fc; }
@media (max-width: 768px) { .main-title { font-size: 2.25rem; } .subtitle { font-size: 1rem; } }
</style>