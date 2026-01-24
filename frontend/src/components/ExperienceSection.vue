<script setup>
const experiences = [
  {
    period: '2020.10 - 2025.03',
    role: '机械工程博士 (PhD)',
    org: '谢菲尔德大学 (University of Sheffield)',
    desc: '研究课题：TFP复合材料力学性能与损伤行为的多尺度表征与建模框架。导师：Dr Christophe Pinna 等。核心贡献：利用SEM和XCT研究TFP失效机制；开发多尺度模型预测强度；开发Python/C++ DVC算法验证模型。'
  },
  {
    period: '2021 - 2025',
    role: '助教 (Teaching Assistant)',
    org: '谢菲尔德大学 (University of Sheffield)',
    desc: '负责有限元分析工业应用、材料完整性、肌肉骨骼系统计算生物力学等课程的辅导与实验指导。多次获得学生好评。'
  },
  {
    period: '2020 - 2025',
    role: 'XCT 实验室管理员 & 培训师',
    org: '谢菲尔德大学 (University of Sheffield)',
    desc: '负责XCT实验室的日常运营与安全合规。培训博士生及研究人员使用XCT设备及数据处理，协助进行复合材料表征实验。'
  },
  {
    period: '2019.09 - 2020.09',
    role: '机械工程理学硕士 (MSc)',
    org: '谢菲尔德大学 (University of Sheffield)',
    desc: '获 Distinction 学位。研究课题：航天器管道组件动态阻尼方法研究。利用ANSYS进行动态仿真与模态分析，使用MATLAB/Python自动化数据处理。'
  },
  {
    period: '2018.09 - 2019.06',
    role: '机械工程工学学士 (BEng)',
    org: '西苏格兰大学 (University of the West of Scotland)',
    desc: '获一等荣誉学位 (First Class Honours)。研究课题：亚麻/碳纤维环氧层合板机械性能研究。进行DCB和三点弯曲等机械测试。'
  },
  {
    period: '2015.09 - 2019.06',
    role: '机械设计制造及其自动化 (本科)',
    org: '长春工程学院',
    desc: '工程学基础教育。'
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
