<template>
  <div class="app">
    <Header />
    <main class="main">
      <JobList :jobs="jobs" />
    </main>
    <Footer />
  </div>
</template>

<script>
import Header from './components/HeaderComponent.vue'
import JobList from './components/JobList.vue'
import Footer from './components/FooterComponent.vue'

export default {
  components: {
    Header,
    JobList,
    Footer
  },
  data() {
    return {
      jobs: []
    }
  },
  async created() {
    
    const response = await fetch('https://jobhive-back.herokuapp.com/api/jobs')
    const data = await response.json()
    this.jobs = data
  }
}
</script>

<style>
.app {
  display: grid;
  grid-template-rows: auto 1fr auto;
  min-height: 100vh;
  font-family: Arial, sans-serif;
}

.main {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  grid-gap: 20px;
  padding: 20px;
}
</style>
