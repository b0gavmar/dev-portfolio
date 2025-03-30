<script setup>
import { ref, onMounted } from 'vue'

const theme = ref('')
const isDarkMode = ref(false)

function setActive(section) {
  active.value = section
}
const toggleTheme = () => {
  isDarkMode.value = !isDarkMode.value
  document.body.classList.toggle('dark-mode', isDarkMode.value)
}

onMounted(() => {
  const stored = localStorage.getItem('darkMode')
  if (stored === 'true') {
    isDarkMode.value = true
    document.body.classList.add('dark-mode')
  }
})
</script>

<template>
  <nav class="navbar navbar-expand-lg navbar-dark">
    <div>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarNav"
        aria-controls="navbarNav"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav ms-auto fs-5">
          <li class="my-auto">
            <button @click="toggleTheme()" class="btn btn-light">
              <div class="bi-moon-fill"></div>
            </button>
          </li>
          <li class="nav-item">
            <a
              class="nav-link"
              :class="{ active: activeSection === 'about' }"
              href="#aboutme"
              @click="setActive('about')"
            >
              About Me
            </a>
          </li>
          <li class="nav-item">
            <a
              class="nav-link"
              :class="{ active: activeSection === 'technologies' }"
              href="#technologies"
              @click="setActive('technologies')"
            >
              Technologies
            </a>
          </li>
          <li class="nav-item">
            <a
              class="nav-link"
              :class="{ active: activeSection === 'projects' }"
              href="#projects"
              @click="setActive('projects')"
            >
              Projects
            </a>
          </li>
          <li class="nav-item">
            <a
              class="nav-link"
              :class="{ active: activeSection === 'schools' }"
              href="#schools"
              @click="setActive('schools')"
            >
              Schools
            </a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<style scoped>
nav {
  display: flex;
  align-items: center;
}

nav a {
  text-decoration: none;
  color: white;
  transition:
    background-color 0.3s ease,
    transform 0.2s ease;
}

nav a:hover {
  background-color: rgba(255, 255, 255, 0.2);
  color: white;
  transform: translateY(-2px);
}

.nav-link.active {
  background-color: rgba(255, 255, 255, 0.3);
  font-weight: 600;
  color: white;
}
</style>
