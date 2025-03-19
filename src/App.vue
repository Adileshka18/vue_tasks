<template>
  <div>
    <!-- Задание 1 -->
    <ul>
      <li v-for="(value, key) in users" :key="key">{{ value }}</li>
    </ul>

    <!-- Задание 2 -->
    <ul>
      <li v-for="(value, key) in users" :key="key">{{ key }} - {{ value }}</li>
    </ul>

    <!-- Задание 3 -->
    <ul>
      <li v-for="(value, key, index) in users" :key="key">{{ key }} - {{ value }} - {{ index }}</li>
    </ul>

    <!-- Задание 4 -->
    <ul>
      <li v-for="(value, key, index) in users" :key="key">{{ key }} - {{ value }} - {{ index + 1 }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      users: {
        user1: '100$',
        user2: '200$',
        user3: '300$'
      }
    };
  }
}
</script>