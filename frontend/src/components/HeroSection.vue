<script setup>
import { Mail, Github, FileText } from 'lucide-vue-next'
</script>

<template>
  <section class="section hero">
    <div class="container hero-content">
      <div class="hero-text">
        <h1>Hello, I'm <span class="highlight">孙国文</span></h1>
        <h2 class="subtitle">机械工程博士 / 研究员</h2>
        <p class="intro">
          专注于先进复合材料的多尺度建模与实验表征。
          擅长利用有限元分析 (ABAQUS)、X射线计算机断层扫描 (XCT) 和数字体积相关技术 (DVC) 解决复杂的工程问题。
          具备丰富的生物力学应用迁移经验，致力于连接实验观测与数值模拟。
        </p>
        <div class="social-links">
          <a href="#" class="btn btn-primary">
            <FileText size="18" /> 查看简历
          </a>
          <a href="https://github.com" target="_blank" class="btn btn-outline">
            <Github size="18" /> GitHub
          </a>
          <a href="mailto:govensun53@gmail.com" class="btn btn-outline">
            <Mail size="18" /> 联系我
          </a>
        </div>
      </div>
      <!-- Placeholder for profile image -->
      <!-- <div class="hero-image">
        <img src="/path/to/profile.jpg" alt="Profile" />
      </div> -->
    </div>
  </section>
</template>

<style scoped>
.hero {
  background-color: var(--bg-secondary);
  padding: 6rem 0;
}

.hero-content {
  max-width: 800px;
  text-align: center; /* Centered for academic clean look */
  margin: 0 auto;
}

.highlight {
  color: var(--accent-color);
}

.subtitle {
  font-size: 1.5rem;
  color: var(--text-secondary);
  font-weight: 400;
  font-family: var(--font-main);
  margin-bottom: 1.5rem;
}

.intro {
  font-size: 1.1rem;
  color: var(--text-secondary);
  margin-bottom: 2.5rem;
  max-width: 600px;
  margin-left: auto;
  margin-right: auto;
}

.social-links {
  display: flex;
  justify-content: center;
  gap: 1rem;
}

.btn {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  padding: 0.75rem 1.5rem;
  border-radius: 4px;
  font-weight: 500;
  text-decoration: none;
  transition: all 0.2s;
}

.btn-primary {
  background-color: var(--primary-color);
  color: white;
  border: 1px solid var(--primary-color);
}

.btn-primary:hover {
  background-color: #1a252f;
  color: white;
  text-decoration: none;
}

.btn-outline {
  background-color: transparent;
  color: var(--text-primary);
  border: 1px solid var(--border-color);
}

.btn-outline:hover {
  border-color: var(--primary-color);
  color: var(--primary-color);
  text-decoration: none;
}
</style>
