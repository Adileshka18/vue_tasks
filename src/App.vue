<template>
  <div>
    <table border="1">
      <thead>
        <tr>
          <th>Name</th>
          <th>Surname</th>
          <th>Age</th>
        </tr>
      </thead>
      <tbody>
        <employee
          v-for="user in users"
          :key="user.id"
          :name="user.name"
          :surname="user.surname"
          :age="user.age"
        />
      </tbody>
    </table>
  </div>
</template>

<script>
import Employee from './components/Employee.vue';

export default {
  components: {
    Employee,
  },
  data() {
    return {
      users: [
        { id: 1, name: 'John', surname: 'Doe', age: 30 },
        { id: 2, name: 'Jane', surname: 'Smith', age: 40 },
        { id: 3, name: 'Jake', surname: 'Johnson', age: 50 },
      ],
    };
  },
};
</script>
