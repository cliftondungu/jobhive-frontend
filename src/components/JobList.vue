<template>
    <div class="job-list-container">
      <div class="job-list">
        <ul class="job-listings">
          <h1>Job Listings</h1>
          <li v-for="job in jobs" :key="job._id" class="job-listing">
            <h2><i class="fas fa-briefcase"></i> {{ job.title }}</h2>
            <p class="job-info"><i class="fas fa-file-alt"></i> Description: {{ job.description }}</p>
            <p class="job-info"><i class="fas fa-map-marker-alt"></i> Location: {{ job.location }}</p>
            <p class="job-info"><i class="fas fa-money-bill"></i> Salary: {{ job.salary }}</p>
            
            <p class="job-description"><i class="fas fa-tasks"></i> Requirements: {{ job.requirements }}</p>
          </li>
        </ul>
      </div>
    </div>
  </template>
  
  <script>
    export default {
      props: {
        jobs: {
          type: Array,
          required: true,
        },
      },
    };
  </script>
  
  <style>
    /* Include the Font Awesome library */
    @import url('https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css');
  
    .job-list-container {
      display: flex;
      justify-content: center;
      align-items: center;
    }
  
    .job-list {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      grid-gap: 20px;
      padding: 20px;
    }
  
    .job-listings {
      list-style: none;
      margin: 0;
      padding: 0;
    }
  
    .job-listing {
      background-color: #f7f7f7;
      border: 1px solid #ccc;
      border-radius: 5px;
      box-shadow: 0 0 5px rgba(0, 0, 0, 0.1);
      padding: 20px;
      margin-bottom: 10px;
    }
  
    .job-listing h2 {
      margin-top: 0;
    }
  
    .job-info {
      font-style: italic;
    }
  
    .job-description {
      font-weight: bold;
      margin-top: 20px;
    }

      .job-info i,
  .job-description i {
    padding-right: 10px;
  }
  </style>
  