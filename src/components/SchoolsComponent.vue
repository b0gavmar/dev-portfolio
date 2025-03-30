<script setup>
const schools = [
  {
    title: 'SZESZC Vasvári Pál',
    description:
      'IT vocational school'
  }
]
</script>


<template>
  <div class="container py-5">
    <h2 class="text-center mb-5 text-primary">Schools I've attended to</h2>
    <div class="row g-4 justify-content-center">
      <div
        v-for="(school, index) in schools"
        :key="index"
        class="col-md-4"
      >
        <div class="card h-100 shadow-sm infocard">
          <div class="card-body d-flex flex-column">
            <h5 class="card-title text-primary">{{ school.title }}</h5>
            <p class="card-text flex-grow-1">{{ school.description }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>

</style>
