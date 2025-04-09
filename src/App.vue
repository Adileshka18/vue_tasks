<template>
  <div>
    <p :class="obj">Этот абзац будет иметь классы в зависимости от значений в объекте.</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      obj: {
        done: true,
        selected: false,
      },
    };
  },
};
</script>

<style scoped>
.done {
  color: green;
}

.selected {
  background-color: yellow;
}
</style>