<script setup>
</script>

<template>
  <div class="container py-5">
    <div class="row g-4 justify-content-center">
      <div class="col-md-5">
        <div class="card h-100 shadow-sm tech-card">
          <div class="card-body">
            <h4 class="card-title text-primary">Technologies I'm most familiar with</h4>
            <p class="card-text">
              HTML, CSS, JS, C# (WPF, Backend), Vue.js, MySQL, Git (Conflict handling, Version control, Git Bash)
            </p>
          </div>
        </div>
      </div>
      <div class="col-md-5">
        <div class="card h-100 shadow-sm tech-card">
          <div class="card-body">
            <h4 class="card-title text-primary">Technologies I've used</h4>
            <p class="card-text">
              Python, C# (Maui, Blazor, WinForms), Node.js, Java, JWT, jQuery, Linux (Ubuntu), Cisco Packet Tracer
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.tech-card {
  border-radius: 12px;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}
.tech-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.15);
}
</style>