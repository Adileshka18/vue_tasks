<!-- Employee.vue -->
<template>
    <div>
      <p>Name: {{ name }}</p>
      <p>Salary: {{ salary }}</p>
      <p>Age: {{ age }}</p>
      <button @click="remove">Remove</button>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      name: String,
      salary: Number,
      age: Number
    },
    methods: {
      remove() {
        this.$emit('remove');
      }
    }
  };
  </script>