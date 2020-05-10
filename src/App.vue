<template>
  <div id="app" class="small-container">
    <h1>Patients</h1>

    <patient-table :patients="patients" />
    <create-patient/>
    
  </div>
</template>

<script>
import PatientTable from './components/PatientTable.vue'
import CreatePatient from './components/CreatePatient.vue'


export default {
  name: 'App',
  components: {
    PatientTable,
    CreatePatient
  },
  data() {
    return {
      patients: []
    }
  },
  mounted() {
    this.getPatients();
  },
  methods: {
    async getPatients() {
      try {
        const response = await fetch('https://jsonplaceholder.typicode.com/users')
        const data = await response.json()
        this.patients = data
      } catch (error) {
        console.error(error)
      }
    }
     
}
}
</script>

<style>
  button {
    background: #009435;
    border: 1px solid #009435;
  }

  .small-container {
    max-width: 680px;
  }
</style>
