<template>
  <div>
    <!-- Задание 1 -->
    <textarea v-model="text" placeholder="Введите текст"></textarea>
    <p>{{ text }}</p>

    <!-- Задание 2 -->
    <textarea v-model="textArea" placeholder="Введите текст"></textarea>
    <button @click="displayWords">Показать слова</button>
    <ul>
      <li v-for="(word, index) in words" :key="index">{{ word }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      text: '',
      textArea: '',
      words: [],
    };
  },
  methods: {
    displayWords() {
      this.words = this.textArea.split(' ');
    },
  },
};
</script>