<script>
export default {
  data() {
    return {
      count: 30
    };
  },
};
</script>

<template>
  <p v-for="num in count" :key="num">
    {{ num }}
  </p>
</template>