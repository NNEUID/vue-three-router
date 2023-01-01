<template>
  <h1>Jobs</h1>
  <div v-for="job in jobs" :key="job.id">
    <span>Title: {{ job.title }}</span> <br>
    <span>Description: {{ job.description }}</span> <br>
  </div>
</template>

<script>
export default {
  data() {
    return {
      jobs: [
        { title: 'Job 1', id: 1, description: 'Lorem' },
        { title: 'Job 2', id: 2, description: 'Lorem' },
        { title: 'Job 3', id: 3, description: 'Lorem' },
      ]
    }

  }
}
</script>

<style>

</style>