<script setup>
import { RouterLink } from 'vue-router'
</script>

<template>
  <nav class="navbar">
    <div class="container navbar-content">
      <RouterLink to="/" class="logo">Scholar.</RouterLink>
      <div class="nav-links">
        <RouterLink to="/">首页</RouterLink>
        <a href="#about">关于</a>
        <a href="#experience">经历</a>
        <a href="#publications">论文</a>
        <a href="#projects">项目</a>
        <!-- <RouterLink to="/blog">博客</RouterLink> -->
      </div>
    </div>
  </nav>
</template>

<style scoped>
.navbar {
  background-color: var(--bg-primary);
  border-bottom: 1px solid var(--border-color);
  position: sticky;
  top: 0;
  z-index: 100;
  padding: 1rem 0;
}

.navbar-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  font-family: var(--font-serif);
  font-size: 1.5rem;
  font-weight: 700;
  color: var(--primary-color);
  text-decoration: none;
}

.nav-links {
  display: flex;
  gap: 2rem;
}

.nav-links a {
  color: var(--text-secondary);
  font-weight: 500;
}

.nav-links a:hover, .nav-links a.router-link-active {
  color: var(--primary-color);
  text-decoration: none;
}
</style>
