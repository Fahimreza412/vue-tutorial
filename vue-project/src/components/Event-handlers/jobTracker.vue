// JobTracker.vue
<script setup>
import { ref, reactive, computed } from 'vue'

// Using ref for primitive values
const totalApplications = ref(0)
const isLoading = ref(false)

// Using reactive for complex objects/arrays
const jobApplications = reactive({
  list: [
    {
      id: 1,
      company: 'Tech Corp',
      position: 'Frontend Developer',
      status: 'Applied',
      appliedDate: '2025-02-10',
      followUpDate: null,
      notes: ''
    }
  ],
  filters: {
    status: 'All',
    dateRange: 'Last 30 days'
  }
})

// Computed property using reactive data
const filteredApplications = computed(() => {
  if (jobApplications.filters.status === 'All') {
    return jobApplications.list
  }
  return jobApplications.list.filter(job => job.status === jobApplications.filters.status)
})

// Methods using both ref and reactive
const addNewApplication = (applicationData) => {
  isLoading.value = true
  
  try {
    const newApplication = {
      id: Date.now(),
      ...applicationData,
      appliedDate: new Date().toISOString().split('T')[0],
      status: 'Applied',
      followUpDate: null
    }
    
    jobApplications.list.push(newApplication)
    totalApplications.value++
  } catch (error) {
    console.error('Error adding application:', error)
  } finally {
    isLoading.value = false
  }
}

const updateApplicationStatus = (id, newStatus) => {
  const application = jobApplications.list.find(app => app.id === id)
  if (application) {
    application.status = newStatus
    if (newStatus === 'Interview Scheduled') {
      application.followUpDate = new Date().toISOString().split('T')[0]
    }
  }
}

const addFollowUpNote = (id, note) => {
  const application = jobApplications.list.find(app => app.id === id)
  if (application) {
    application.notes += `[${new Date().toLocaleDateString()}] ${note}\n`
  }
}

const updateFilters = (newFilters) => {
  Object.assign(jobApplications.filters, newFilters)
}
</script>

<template>
  <div class="job-tracker">
    <div class="stats">
      <p>Total Applications: {{ totalApplications }}</p>
      <p>Active Applications: {{ filteredApplications.length }}</p>
    </div>

    <div class="filters">
      <select v-model="jobApplications.filters.status">
        <option>All</option>
        <option>Applied</option>
        <option>Interview Scheduled</option>
        <option>Rejected</option>
        <option>Offer Received</option>
      </select>
    </div>

    <div class="applications-list" v-if="!isLoading">
      <div v-for="app in filteredApplications" :key="app.id" class="application-card">
        <h3>{{ app.company }}</h3>
        <p>Position: {{ app.position }}</p>
        <p>Status: {{ app.status }}</p>
        <p>Applied: {{ app.appliedDate }}</p>
        <p v-if="app.followUpDate">Follow-up: {{ app.followUpDate }}</p>
        <textarea v-model="app.notes" placeholder="Add notes..."></textarea>
        <div class="actions">
          <button @click="updateApplicationStatus(app.id, 'Interview Scheduled')">
            Schedule Interview
          </button>
          <button @click="addFollowUpNote(app.id, 'Sent follow-up email')">
            Add Follow-up
          </button>
        </div>
      </div>
    </div>
    
    <div v-else class="loading">
      Loading...
    </div>
  </div>
</template>

<style scoped>
.job-tracker {
  padding: 20px;
}

.application-card {
  border: 1px solid #ddd;
  padding: 15px;
  margin: 10px 0;
  border-radius: 4px;
}

.actions {
  margin-top: 10px;
}

textarea {
  width: 100%;
  min-height: 60px;
  margin: 10px 0;
}
</style>