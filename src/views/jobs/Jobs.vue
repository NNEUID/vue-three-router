<template>
  <h1>Jobs</h1>
  <div v-if="jobs.length">
    <div v-for="job in jobs" :key="job.id" class="job">
      <router-link :to="{ name: 'jobdetails', params: { id: job.id } }">
        <h2>Title: {{ job.title }}</h2>
      </router-link>
    </div>
    <div>
      Loading...
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      jobs: [

      ]
    }

  },
  mounted() {
    fetch('http://localhost:3000/jobs').then(res => res.json()).then(data => this.jobs = data).catch(error => console.log(error))
  }
}
</script>

<style>
.job h2 {
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