<template>
  <div>
    <button @click="emitEvent">Click me</button>
  </div>
</template>

<script>
export default {
  methods: {
    emitEvent() {
      this.$emit('customEvent', 'Event data');
    }
  }
};
</script>