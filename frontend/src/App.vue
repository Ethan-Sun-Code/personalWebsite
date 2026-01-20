<script setup>
import NavBar from './components/NavBar.vue'
</script>

<template>
  <div class="app-container">
    <NavBar />
    <RouterView />
    <footer class="footer">
      <p>&copy; 2026 Academic Portfolio. All rights reserved.</p>
    </footer>
  </div>
</template>

<style scoped>
.app-container {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

.footer {
  margin-top: auto;
  padding: 2rem;
  text-align: center;
  background-color: var(--bg-secondary);
  color: var(--text-secondary);
  font-size: 0.9rem;
  border-top: 1px solid var(--border-color);
}
</style>
