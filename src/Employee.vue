<!-- Employee.vue -->
<template>
    <div>
      <button @click="sendWorkerData(worker.name)">Send Name</button>
    </div>
  </template>
  
  <script>
  export default {
    props: ['worker', 'sendData'],
    methods: {
      sendWorkerData(name) {
        this.sendData(name);
      }
    }
  };
  </script>