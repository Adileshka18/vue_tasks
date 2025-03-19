<script>
export default {
  data() {
    return {
      arr: ['x', 'y', 'z'],
    };
  },
};
</script>

<template>
  <ul>
    <li v-for="(elem, key) in arr" :key="key">{{ key }}</li>
  </ul>
</template>
