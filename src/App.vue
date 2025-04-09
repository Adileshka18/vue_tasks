<!-- Employee.vue -->
<template>
  <tr>
    <td>{{ employee.name }}</td>
    <td>{{ employee.salary }}</td>
    <td>{{ employee.age }}</td>
    <td>
      <a href="#" @click="removeEmployee">Delete</a>
    </td>
    <td>
      <a href="#" @click="editEmployee">Edit</a>
    </td>
  </tr>
</template>

<script>
export default {
  props: {
    employee: Object,
    index: Number,
  },
  methods: {
    removeEmployee() {
      this.$emit('remove', this.index);
    },
    editEmployee() {
      this.$emit('edit', this.index);
    },
  },
};
</script>