<script>
export default {
  data() {
    return {
      visible: true,
    };
  },

  methods: {
    show() {
      this.visible = true;
    },
    hide() {
      this.visible = false;
    }
  }
};
</script>

<template>
  <button v-if="!visible" @click="show">Показать</button>
  <button v-if="visible" @click="hide">Скрыть</button>
  <p v-if="visible">text</p>
</template>