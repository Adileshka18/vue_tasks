<script>
export default {
  data() {
    return {
      visible: [false, false, false],
    };
  },
};
</script>

<template>
  <div>
    <button @click="visible[0] = !visible[0]">Toggle 1</button>
    <p v-if="visible[0]">Text 1</p>

    <button @click="visible[1] = !visible[1]">Toggle 2</button>
    <p v-if="visible[1]">Text 2</p>

    <button @click="visible[2] = !visible[2]">Toggle 3</button>
    <p v-if="visible[2]">Text 3</p>
  </div>
</template>