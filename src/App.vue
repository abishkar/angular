<template>
  <div id="app" class="small-container">
    <h1>Patients</h1>

    <patient-table :patients="patients" />
  </div>
</template>

<script>
import PatientTable from './components/PatientTable.vue'

export default {
  name: 'App',
  components: {
    PatientTable
  },
  data() {
    return {
      patients: [
        {
          id: 1,
          name: 'Richard Hendricks',
          email: 'richard@piedpiper.com',
        },
        {
          id: 2,
          name: 'Bertram Gilfoyle',
          email: 'gilfoyle@piedpiper.com',
        },
        {
          id: 3,
          name: 'Dinesh Chugtai',
          email: 'dinesh@piedpiper.com',
        },
      ],
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
