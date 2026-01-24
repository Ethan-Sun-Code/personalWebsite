<script setup>
import { ExternalLink, Github } from 'lucide-vue-next'

const projects = [
  {
    title: 'TFP 复合材料多尺度表征与建模 (PhD)',
    desc: '研究 TFP 复合材料的力学性能与损伤行为。利用 SEM 和 XCT 进行失效机制研究，开发多尺度有限元模型 (ABAQUS) 预测强度，并使用 Python/C++ 开发 DVC 算法进行验证。',
    tags: ['ABAQUS', 'Python', 'XCT', 'DVC', 'Multiscale Modelling'],
    link: '#',
    github: '#'
  },
  {
    title: '航天器管道组件动态阻尼研究 (MSc)',
    desc: '通过 ANSYS 进行动态仿真与模态分析，探索增加航天器管道组件动态阻尼的方法。使用 MATLAB 和 Python 自动化数据处理流程。',
    tags: ['ANSYS', 'MATLAB', 'Python', 'Dynamics'],
    link: '#',
    github: '#'
  },
  {
    title: '亚麻/碳纤维混合复合材料力学性能研究 (BEng)',
    desc: '评估湿热环境下亚麻/碳纤维环氧层合板的弯曲强度和层间断裂韧性。进行 DCB 和三点弯曲实验。',
    tags: ['Mechanical Testing', 'Composites', 'Sustainability'],
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
