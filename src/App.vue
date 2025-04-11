<template>
  <div>
    <Employee
      v-for="(user, index) in users"
      :key="user.id"
      :name="user.name"
      :salary="user.salary"
      :age="user.age"
      @remove="removeUser(index)"
      @edit="editUser(index)"
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
      users: [
        {
          id: 1,
          name: 'name1',
          salary: 100,
          age: 30
        },
        {
          id: 2,
          name: 'name2',
          salary: 200,
          age: 40
        },
        {
          id: 3,
          name: 'name3',
          salary: 300,
          age: 50
        }
      ]
    };
  },
  methods: {
    removeUser(index) {
      this.users.splice(index, 1);
    },
    editUser(index) {
      const user = this.users[index];
      const newName = prompt('Edit name:', user.name);
      const newSalary = prompt('Edit salary:', user.salary);
      const newAge = prompt('Edit age:', user.age);

      if (newName !== null) user.name = newName;
      if (newSalary !== null) user.salary = parseFloat(newSalary);
      if (newAge !== null) user.age = parseInt(newAge);
    }
  }
};
</script>