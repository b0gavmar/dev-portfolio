<script setup>
import { RouterLink, RouterView } from 'vue-router'
import TechnologiesComponent from './components/TechnologiesComponent.vue';
import ProjectsComponent from './components/ProjectsComponent.vue';
import Navbar from './components/Navbar.vue';
import About from './components/About.vue';
</script>

<template>
  <header>
    <Navbar/>
  </header>

  <About/>

  <div class="container-fluid">
    <TechnologiesComponent/>
    <ProjectsComponent />
  </div>


  <footer class="d-flex flex-wrap justify-content-between align-items-center py-3 my-4 border-top">
    <div class="col-md-4 d-flex align-items-center">
      <a href="/" class="mb-3 me-2 mb-md-0 text-body-secondary text-decoration-none lh-1">
        <svg class="bi" width="30" height="24"><use xlink:href="#bootstrap"></use></svg>
      </a>
      <span class="mb-3 mb-md-0 text-body-secondary">© 2025 Martin Gavlik</span>
    </div>

    <ul class="nav col-md-4 justify-content-end list-unstyled d-flex">
      <li class="ms-3"><a class="text-body-secondary" href="#"><svg class="bi" width="24" height="24"><use xlink:href="#github">Github</use></svg></a></li>
      <li class="ms-3"><a class="text-body-secondary" href="#"><svg class="bi" width="24" height="24"><use xlink:href="#email"></use></svg></a></li>
    </ul>
  </footer>
</template>


