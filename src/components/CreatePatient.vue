<template>
  <div id="patient-create">
    
 <form @submit.prevent="handleSubmit">



  <p>
    <label for="name">Patient Name</label>
    <input
      id="name"
      v-model="patient.name"
      type="text"
      name="name"
    >
  </p>

  <p>
    <label for="age">Age</label>
    <input
      id="age"
      v-model="patient.age"
      type="number"
      name="age"
      min="0"
    >
  </p>

  <p>
    <label for="service">Service Type</label>
    <select
      id="service"
      v-model="service"
      name="service"
    >
      <option>Basic Care</option>
      <option>Intermediate Care</option>
      <option>Advanced Care</option>
    </select>
  </p>

  <p>
    <button>Add Patient</button>
  </p>

</form>


  </div>
</template>

<script>
  export default {
    name: 'create-patient',
    
    data() {
    return {
      patient: {
        name: '',
        age: '',
      }
    }
  }
,

methods: {
    handleSubmit: function () {
    console.log(this.patient);   
    this.patient.name;
    this.patient.age;
    }



  }
  }
</script>

<style scoped></style>