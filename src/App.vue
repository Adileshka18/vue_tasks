<template>
  <div>
    <button @click="showCurrentDate">Показать текущую дату</button>
  </div>
</template>

<script>
export default {
  methods: {
    showCurrentDate() {
      const currentDate = new Date();
      alert(`Текущая дата: ${currentDate.toLocaleString()}`);
    }
  }
}
</script>