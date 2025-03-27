<template>
    <nav>
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/about">About</RouterLink>
      <RouterLink to="/technologies">Technologies</RouterLink>
      <RouterLink to="/ides">IDEs</RouterLink>
      <RouterLink to="/projects">Projects</RouterLink>
    </nav>
</template>
<style scoped>



nav {
  display: flex;
  align-items: center;
  gap: 1rem;
}

nav a {
  text-decoration: none;
  color: white;
  font-weight: 500;
  padding: 0.6rem 1.2rem;
  border-radius: 8px;
  transition: background-color 0.3s ease, transform 0.2s ease;
}

nav a:hover {
  background-color: rgba(255, 255, 255, 0.2);
  transform: translateY(-2px);
}

nav a.router-link-exact-active {
  background-color: rgba(255, 255, 255, 0.3);
  font-weight: 600;
}


</style>