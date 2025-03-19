<script>
export default {
  data() {
    return {
      items: [1, 2, 3, 4, 5],
    };
  },
};
</script>

<template>
  <ul>
    <li v-for="elem in items" :key="elem">{{ elem* elem }}</li>
  </ul>
</template>
