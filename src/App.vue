<template>
  <div>
    <p class="green-text-yellow-background">Текст с зеленым цветом и желтым фоном</p>
    <p class="bold-italic-text">Текст жирный и курсивный</p>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
};
</script>

<style scoped>
.green-text-yellow-background {
  color: green;
  background-color: yellow;
}

.bold-italic-text {
  font-weight: bold;
  font-style: italic;
}
</style>