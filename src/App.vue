<template>
  <div>
    <!-- Задание 1: Добавление нового элемента в конец списка -->
    <h3>Задание 1</h3>
    <ul>
      <li v-for="(item, index) in items1" :key="index">{{ item }}</li>
    </ul>
    <button @click="addItem">Добавить элемент</button>

    <!-- Задание 2: Удаление первого элемента списка -->
    <h3>Задание 2</h3>
    <ul>
      <li v-for="(item, index) in items2" :key="index">{{ item }}</li>
    </ul>
    <button @click="removeFirstItem">Удалить первый элемент</button>

    <!-- Задание 3: Удаление последнего элемента списка -->
    <h3>Задание 3</h3>
    <ul>
      <li v-for="(item, index) in items3" :key="index">{{ item }}</li>
    </ul>
    <button @click="removeLastItem">Удалить последний элемент</button>

    <!-- Задание 4: Удаление предпоследнего элемента списка -->
    <h3>Задание 4</h3>
    <ul>
      <li v-for="(item, index) in items4" :key="index">{{ item }}</li>
    </ul>
    <button @click="removeSecondLastItem">Удалить предпоследний элемент</button>

    <!-- Задание 5: Сортировка элементов списка -->
    <h3>Задание 5</h3>
    <ul>
      <li v-for="(item, index) in items5" :key="index">{{ item }}</li>
    </ul>
    <button @click="sortItems">Отсортировать</button>

    <!-- Задание 6: Обращение порядка элементов списка -->
    <h3>Задание 6</h3>
    <ul>
      <li v-for="(item, index) in items6" :key="index">{{ item }}</li>
    </ul>
    <button @click="reverseItems">Обратить порядок</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      // Задание 1
      items1: ['Item 1', 'Item 2', 'Item 3'],
      // Задание 2
      items2: ['Item 1', 'Item 2', 'Item 3'],
      // Задание 3
      items3: ['Item 1', 'Item 2', 'Item 3'],
      // Задание 4
      items4: ['Item 1', 'Item 2', 'Item 3'],
      // Задание 5
      items5: ['Item 3', 'Item 1', 'Item 2'],
      // Задание 6
      items6: ['Item 1', 'Item 2', 'Item 3']
    };
  },
  methods: {
    // Задание 1
    addItem() {
      this.items1.push('New Item');
    },
    // Задание 2
    removeFirstItem() {
      this.items2.shift();
    },
    // Задание 3
    removeLastItem() {
      this.items3.pop();
    },
    // Задание 4
    removeSecondLastItem() {
      if (this.items4.length > 1) {
        this.items4.splice(this.items4.length - 2, 1);
      }
    },
    // Задание 5
    sortItems() {
      this.items5.sort();
    },
    // Задание 6
    reverseItems() {
      this.items6.reverse();
    }
  }
};
</script>

<style scoped>
ul {
  list-style-type: none;
}

li {
  margin: 5px 0;
}

button {
  margin-top: 10px;
}
</style>