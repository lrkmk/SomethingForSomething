<script setup lang="ts">
import { ref } from 'vue';

const projects = ['Project 1', 'Project 2', 'Project 3'];
const selectedProject = ref(projects[0]);
</script>

<template>
  <div class="app-container">
    <div class="sidebar">
      <h2>Projects</h2>
      <select v-model="selectedProject">
        <option v-for="project in projects" :key="project" :value="project">
          {{ project }}
        </option>
      </select>
    </div>
    <div class="main-content">
      <h1>{{ selectedProject }}</h1>
      <p>Content for {{ selectedProject }} will be displayed here.</p>
    </div>
  </div>
</template>

<style scoped>
.app-container {
  display: flex;
  height: 100vh;
}

.sidebar {
  width: 200px;
  padding: 20px;
  background-color: #f4f4f4;
  border-right: 1px solid #ddd;
}

.main-content {
  flex-grow: 1;
  padding: 20px;
}

select {
  width: 100%;
  padding: 8px;
  margin-top: 10px;
}
</style>
