<script>
export default {
  data() {
    return {
      isChecked: false,
    };
  },
};
</script>

<template>
  <div>
    <input type="checkbox" v-model="isChecked" />
    <p v-if="isChecked">Абзац отображается, потому что checkbox отмечен.</p>
  </div>
</template>
