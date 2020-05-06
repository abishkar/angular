<template>
  <div id="patient-table">
    <table>
     <thead>
        <tr>
          <th>Patient name</th>
          <th>Patient email</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="patient in patients" :key="patient.id">
          <td>{{ patient.name }}</td>
          <td>{{ patient.email }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
  export default {
    name: 'patient-table',
    props: {
    patients: Array,
  },
  }
</script>

<style scoped></style>