<template>
  <div>
    <Employee :name="name" :salary="salary" :age="age" />
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
      name: 'John Doe',
      salary: 5000,
      age: 30
    };
  }
};
</script>