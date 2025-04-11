<template>
  <div>
    <Employee 
      :worker="worker" 
      :sendData="sendData" 
    />
  </div>
</template>

<script>
import Employee from './Employee.vue';

export default {
  components: {
    Employee
  },
  data() {
    return {
      worker: {
        name: 'John',
        salary: 5000
      }
    };
  },
  methods: {
    sendData(name) {
      console.log(name);
    }
  }
};
</script>