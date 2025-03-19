<script>
export default {
  data() {
    return {
      isAuth: true,
    };
  },
};
</script>

<template>
  <div>
    <button @click="isAuth = !isAuth">Toggle</button>
    <p v-show="isAuth">+++</p>
  </div>
</template>
