<template>
  <div>
    <p :class="cssClasses">Это абзац с динамическими классами.</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cssClasses: ['class1', 'class2', 'class3']
    };
  }
};
</script>

<style scoped>
.class1 {
  color: red;
}

.class2 {
  font-weight: bold;
}

.class3 {
  font-size: 20px;
}
</style>