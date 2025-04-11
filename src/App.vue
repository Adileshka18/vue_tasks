<template>
  <div>
    <form @submit.prevent="addUser">
      <div>
        <label for="name">Name:</label>
        <input v-model="newUser.name" id="name" type="text" required />
      </div>
      <div>
        <label for="salary">Salary:</label>
        <input v-model="newUser.salary" id="salary" type="number" required />
      </div>
      <div>
        <label for="age">Age:</label>
        <input v-model="newUser.age" id="age" type="number" required />
      </div>
      <button type="submit">Add Worker</button>
    </form>

    <div v-for="(user, index) in users" :key="user.id">
      <Employee
        :name="user.name"
        :salary="user.salary"
        :age="user.age"
        @remove="removeUser(index)"
        @edit="editUser(index)"
      />
    </div>
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
      newUser: {
        name: '',
        salary: '',
        age: ''
      },
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
    addUser() {
      if (this.newUser.name && this.newUser.salary && this.newUser.age) {
        const newUser = {
          id: Date.now(),
          name: this.newUser.name,
          salary: parseFloat(this.newUser.salary),
          age: parseInt(this.newUser.age)
        };
        this.users.push(newUser);

        // Reset form fields
        this.newUser.name = '';
        this.newUser.salary = '';
        this.newUser.age = '';
      }
    },
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