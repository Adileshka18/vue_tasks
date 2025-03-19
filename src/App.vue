<template>
  <div>
    <!-- Задание 1 -->
    <div v-for="(item, index) in items" :key="index">
      <p>{{ item }}</p>
      <p class="divider"></p>
    </div>

    <!-- Задание 2 -->
    <ul>
      <li v-for="(item, index) in items" :key="index">
        {{ item }}
        <p v-if="index !== items.length - 1" class="divider"></p>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [1, 2, 3]
    };
  }
}
</script>