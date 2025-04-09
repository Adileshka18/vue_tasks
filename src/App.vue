<template>
  <div>
    <!-- Задание 1 -->
    <input v-model.number="number" type="number" placeholder="Введите число">
    <button @click="calculateSquareRoot">Показать квадратный корень</button>
    <p>{{ squareRoot }}</p>

    <!-- Задание 2 -->
    <input v-model.number="number1" type="number" placeholder="Введите первое число">
    <input v-model.number="number2" type="number" placeholder="Введите второе число">
    <button @click="calculateSum">Показать сумму</button>
    <p>{{ sum }}</p>

    <!-- Задание 3 -->
    <input v-model="text1" type="text" placeholder="Введите текст 1">
    <input v-model="text2" type="text" placeholder="Введите текст 2">
    <button @click="swapText">Поменять тексты</button>
    <p>{{ text1 }}</p>
    <p>{{ text2 }}</p>

    <!-- Задание 4 -->
    <input v-model="fullName" type="text" placeholder="Введите ФИО">
    <button @click="splitName">Разделить ФИО</button>
    <p>{{ surname }}</p>
    <p>{{ name }}</p>
    <p>{{ patronymic }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      number: 0,
      squareRoot: null,
      number1: 0,
      number2: 0,
      sum: 0,
      text1: '',
      text2: '',
      fullName: '',
      surname: '',
      name: '',
      patronymic: '',
    };
  },
  methods: {
    calculateSquareRoot() {
      this.squareRoot = Math.sqrt(this.number);
    },
    calculateSum() {
      this.sum = this.number1 + this.number2;
    },
    swapText() {
      const temp = this.text1;
      this.text1 = this.text2;
      this.text2 = temp;
    },
    splitName() {
      const parts = this.fullName.split(' ');
      this.surname = parts[0] || '';
      this.name = parts[1] || '';
      this.patronymic = parts[2] || '';
    },
  },
};
</script>