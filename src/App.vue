<script setup>
import { RouterLink, RouterView } from 'vue-router'
import TechnologiesComponent from './components/TechnologiesComponent.vue'
import ProjectsComponent from './components/ProjectsComponent.vue'
import Navbar from './components/Navbar.vue'
import About from './components/About.vue'
import Footer from './components/Footer.vue'
import SchoolsComponent from './components/SchoolsComponent.vue'
import AboutMe from './components/AboutMe.vue'
</script>

<template>
  <header>
    <Navbar />
  </header>
  <div id="about">
    <About />
  </div>

  <div class="container-fluid" id="aboutme">
    <AboutMe />
  </div>

  

  <div class="container" id="projects">
    <ProjectsComponent />
  </div>

  <div class="container-fluid" id="technologies">
    <TechnologiesComponent />
  </div>

  <div class="container" id="schools">
    <SchoolsComponent />
  </div>

  <footer
    class="d-flex flex-wrap justify-content-between align-items-center py-3 my-4 border-top mb-0 custombg"
  >
    <Footer />
  </footer>
</template>
