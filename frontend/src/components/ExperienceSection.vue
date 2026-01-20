<script setup>
const experiences = [
  {
    period: '2023 - 至今',
    role: '博士研究生 (PhD Student)',
    org: '某知名大学计算机学院',
    desc: '研究方向：深度学习与自然语言处理。发表顶级会议论文 2 篇。'
  },
  {
    period: '2020 - 2023',
    role: '硕士研究生',
    org: '某科技大学',
    desc: '主修计算机科学与技术，GPA: 3.8/4.0。荣获国家奖学金。'
  },
  {
    period: '2022.06 - 2022.09',
    role: '算法实习生',
    org: '某互联网大厂',
    desc: '负责推荐系统召回模块的优化，提升点击率 5%。'
  }
]
</script>

<template>
  <section id="experience" class="section bg-alt">
    <div class="container">
      <h2 class="section-title">教育 & 经历</h2>
      <div class="timeline">
        <div v-for="(exp, index) in experiences" :key="index" class="timeline-item">
          <div class="timeline-marker"></div>
          <div class="timeline-content card">
            <span class="period">{{ exp.period }}</span>
            <h3 class="role">{{ exp.role }}</h3>
            <h4 class="org">{{ exp.org }}</h4>
            <p class="desc">{{ exp.desc }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.bg-alt {
  background-color: var(--bg-secondary);
}

.timeline {
  position: relative;
  max-width: 800px;
  margin: 0 auto;
  padding-left: 2rem;
}

.timeline::before {
  content: '';
  position: absolute;
  left: 0;
  top: 0;
  bottom: 0;
  width: 2px;
  background-color: var(--border-color);
}

.timeline-item {
  position: relative;
  margin-bottom: 2rem;
}

.timeline-marker {
  position: absolute;
  left: -2rem;
  top: 1.5rem;
  width: 12px;
  height: 12px;
  background-color: var(--accent-color);
  border-radius: 50%;
  transform: translateX(-5px); /* Center on line (2px line, 12px dot -> -5px offset) */
  border: 2px solid white;
}

.timeline-content {
  position: relative;
}

.period {
  display: inline-block;
  font-size: 0.85rem;
  font-weight: 600;
  color: var(--accent-color);
  margin-bottom: 0.5rem;
}

.role {
  font-size: 1.25rem;
  margin-bottom: 0.25rem;
}

.org {
  font-size: 1rem;
  color: var(--text-secondary);
  font-weight: 400;
  font-family: var(--font-main);
  margin-bottom: 1rem;
}

.desc {
  color: var(--text-secondary);
  font-size: 0.95rem;
}
</style>
