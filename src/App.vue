<script>
export default {
  data() {
    return {
      day: new Date().getDay(), // Получаем текущий день недели (0 - воскресенье, 6 - суббота)
    };
  },
};
</script>

<template>
  <div>
    <p v-if="day === 0">Sunday</p>
    <p v-if="day === 1">Monday</p>
    <p v-if="day === 2">Tuesday</p>
    <p v-if="day === 3">Wednesday</p>
    <p v-if="day === 4">Thursday</p>
    <p v-if="day === 5">Friday</p>
    <p v-if="day === 6">Saturday</p>
  </div>
</template>
