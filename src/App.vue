<template>
  <div>
    <!-- Задание 1: Применение объекта с классами для скрытия элемента -->
    <p :class="obj">Этот абзац будет скрыт, если obj.hidden == true</p>

    <!-- Задание 2: Кнопка для показа элемента -->
    <button @click="showElement">Показать элемент</button>

    <!-- Задание 3: Кнопка для скрытия элемента -->
    <button @click="hideElement">Скрыть элемент</button>

    <!-- Задание 4: Кнопка для тогглирования видимости элемента -->
    <button @click="toggleElement">Тогглить элемент</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      obj: {
        hidden: true,  
      },
    };
  },
  methods: {
    showElement() {
      this.obj.hidden = false;  
    },
    hideElement() {
      this.obj.hidden = true;   
    },
    toggleElement() {
      this.obj.hidden = !this.obj.hidden;  
    },
  },
};
</script>

<style scoped>
.hidden {
  display: none; 
}
</style>