<script setup>
import { ExternalLink, Github } from 'lucide-vue-next'

const projects = [
  {
    title: 'Personal Academic Website',
    desc: '基于 Django 和 Vue 3 的前后端分离个人网站，支持 Docker 容器化部署。包含博客管理、项目展示等功能。',
    tags: ['Vue 3', 'Django', 'Docker', 'MySQL'],
    link: '#',
    github: '#'
  },
  {
    title: 'AI Image Classifier',
    desc: '使用 PyTorch 构建的图像分类模型，在 ImageNet 上达到了 85% 的 Top-1 准确率。提供 RESTful API 接口。',
    tags: ['Python', 'PyTorch', 'FastAPI'],
    link: '#',
    github: '#'
  },
  {
    title: 'Smart Home Dashboard',
    desc: '物联网设备可视化仪表盘，实时监控室内温度、湿度及设备状态。支持 MQTT 协议。',
    tags: ['React', 'Node.js', 'MQTT'],
    link: '#',
    github: '#'
  }
]
</script>

<template>
  <section id="projects" class="section">
    <div class="container">
      <h2 class="section-title">项目展示</h2>
      <div class="projects-grid">
        <div v-for="(project, index) in projects" :key="index" class="project-card card">
          <div class="card-header">
            <h3>{{ project.title }}</h3>
            <div class="links">
              <a v-if="project.github" :href="project.github" target="_blank" title="View Code">
                <Github size="18" />
              </a>
              <a v-if="project.link" :href="project.link" target="_blank" title="Live Demo">
                <ExternalLink size="18" />
              </a>
            </div>
          </div>
          <p class="desc">{{ project.desc }}</p>
          <div class="tags">
            <span v-for="tag in project.tags" :key="tag" class="tag">{{ tag }}</span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 2rem;
}

.project-card {
  display: flex;
  flex-direction: column;
  height: 100%;
}

.card-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 1rem;
}

.card-header h3 {
  font-size: 1.25rem;
  margin: 0;
  line-height: 1.4;
}

.links {
  display: flex;
  gap: 0.75rem;
}

.links a {
  color: var(--text-secondary);
}

.links a:hover {
  color: var(--accent-color);
}

.desc {
  color: var(--text-secondary);
  font-size: 0.95rem;
  margin-bottom: 1.5rem;
  flex-grow: 1;
}

.tags {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
}

.tag {
  background-color: #e3f2fd;
  color: var(--accent-color);
  padding: 0.25rem 0.75rem;
  border-radius: 4px;
  font-size: 0.8rem;
  font-weight: 500;
}
</style>
