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
    <template v-if="isAuth">
      <p>+++</p>
      <p>+++</p>
      <p>+++</p>
    </template>
  </div>
</template>
