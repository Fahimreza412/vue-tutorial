<script setup>
  // Define the prop
  const props = defineProps({
    job: {
      type: Object,
      required: true  // Must provide this prop
    }
  });
  
  // Use the prop in logic
  const applyForJob = () => {
    console.log(`Applied for ${props.job.title} at ${props.job.company}`);
  };
  </script>
  
  <style scoped>
  .job-card {
    border: 1px solid #ddd;
    padding: 1rem;
    margin: 1rem 0;
  }
  </style>

<template>
    <div class="job-card">
      <h3>{{ job.title }}</h3>
      <p>Company: {{ job.company }}</p>
      <p>Location: {{ job.location }}</p>
      <p>Salary: {{ job.salary }}</p>
      <button @click="applyForJob">Apply Now</button>
    </div>
  </template>
  
  