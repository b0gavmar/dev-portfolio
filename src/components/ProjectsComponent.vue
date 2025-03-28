<script setup>
const projects = [
  {
    title: 'PipeLine',
    description:
      'An advanced backend system written in C# with RESTful architecture. Handles user authentication, device & charging management, and error ticketing logic.'
  },
  {
    title: 'Portfolio Website',
    description:
      'This very responsive and animated portfolio project, built using Vue 3 and Bootstrap 5.'
  }
]
</script>

<template>
  <div class="container py-5">
    <h2 class="text-center mb-5 text-primary">My Projects</h2>
    <div class="row g-4 justify-content-center">
      <div
        v-for="(project, index) in projects"
        :key="index"
        class="col-md-4"
      >
        <div class="card h-100 shadow-sm project-card">
          <div class="card-body d-flex flex-column">
            <h5 class="card-title text-primary">{{ project.title }}</h5>
            <p class="card-text flex-grow-1">{{ project.description }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.project-card {
  border-radius: 12px;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}
.project-card:hover {
  transform: translateY(-6px);
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.15);
}
</style>
