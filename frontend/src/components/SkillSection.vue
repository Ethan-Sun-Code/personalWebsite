<script setup>
const skills = [
  { category: '计算建模 & 仿真', items: ['ABAQUS (UMAT/VUMAT)', 'Finite Element Analysis', 'Process-Structure-Performance', 'Multiscale Modelling'] },
  { category: '实验表征 & 测试', items: ['X-ray CT (XCT)', 'SEM', 'Digital Volume Correlation (DVC)', 'In-situ Mechanical Testing'] },
  { category: '编程 & 开发', items: ['Python', 'PyQt', 'C++', 'MATLAB', 'Image-based Modelling'] },
  { category: '通用能力', items: ['Project Coordination', 'Data Management', 'Technical Communication', 'Mentoring'] }
]
</script>

<template>
  <section id="about" class="section">
    <div class="container">
      <h2 class="section-title">技术栈 & 能力</h2>
      <div class="skills-grid">
        <div v-for="(skillGroup, index) in skills" :key="index" class="skill-group card">
          <h3>{{ skillGroup.category }}</h3>
          <div class="tags">
            <span v-for="skill in skillGroup.items" :key="skill" class="tag">{{ skill }}</span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.skills-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 1.5rem;
}

.skill-group h3 {
  font-size: 1.2rem;
  margin-bottom: 1rem;
  color: var(--text-primary);
  border-bottom: 1px solid var(--border-color);
  padding-bottom: 0.5rem;
}

.tags {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
}

.tag {
  background-color: var(--bg-secondary);
  color: var(--text-primary);
  padding: 0.25rem 0.75rem;
  border-radius: 15px;
  font-size: 0.9rem;
  border: 1px solid transparent;
}

.card:hover .tag {
  border-color: var(--accent-color);
  color: var(--accent-color);
}
</style>
