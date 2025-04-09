<template>
  <div>
    <button :class="{ valid: isValid, disabled: isDisabled }">
      Кнопка
    </button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isValid: true,
      isDisabled: true,
    };
  },
};
</script>

<style scoped>
.valid {
  background-color: green;
  color: white;
}

.disabled {
  background-color: gray;
  color: darkgray;
  pointer-events: none;
}
</style>