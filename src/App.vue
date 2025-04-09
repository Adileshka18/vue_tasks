<template>
  <div>
    <!-- Задание 1 -->
    <input v-model="text" type="text" placeholder="Введите текст">
    <p>{{ text }}</p>

    <!-- Задание 2 -->
    <input v-model="text" type="text" placeholder="Введите текст">
    <p>{{ text.toUpperCase() }}</p>

    <!-- Задание 3 -->
    <input v-model.number="number" type="number" placeholder="Введите число">
    <p>{{ number * number }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      text: '',
      number: 0,
    };
  },
};
</script>