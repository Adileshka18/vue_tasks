<template>
  <div>
    
    <p :class="cssClasses">Этот абзац будет иметь классы active и valid в зависимости от значений в объекте.</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      
      cssClasses: {
        active: true,
        valid: false,
      },
    };
  },
};
</script>

<style scoped>
.active {
  color: green;
}

.valid {
  font-weight: bold;
}
</style>