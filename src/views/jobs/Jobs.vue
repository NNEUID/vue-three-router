<template>
  <h1>Jobs</h1>
  <div v-for="job in jobs" :key="job.id" class="job">
    <router-link :to="{ name: 'jobdetails', params: { id: job.id } }">
      <h2>Title: {{ job.title }}</h2>
    </router-link>
  </div>
</template>

<script>
export default {
  data() {
    return {
      jobs: [
        { title: 'UX Designer at Open HI', id: 1, description: 'Lorem' },
        { title: 'Frontend Developer at Preggy Health', id: 2, description: 'Lorem' },
        { title: 'DevOps Engineer at Colorbrace LLC', id: 3, description: 'Lorem' },
      ]
    }

  }
}
</script>

<style>
.jobs h2 {
background: #f4f4f4;
padding: 20px;
border-radius: 10px;
margin: 10px auto;
max-width: 600px;
cursor: pointer;
color: #444;
}

.job h2:hover {
  background: #ddd;
}

.job a {
  text-decoration: none;
}
</style>