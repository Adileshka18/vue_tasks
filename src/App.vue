<script>
export default {
  data() {
    return {
      // Задача №1
      inputText: '',
      submittedText: '',

      // Задача №2
      ctrlClickText: '',

      // Задача №3
      mouseClickText: '',
    };
  },
  methods: {
    // Задача №1
    handleKeyPress(event) {
      if (event.key === 'Enter') {
        this.submittedText = this.inputText;
      }
    },

    // Задача №2
    handleCtrlClick(event) {
      if (event.ctrlKey) {
        this.ctrlClickText = 'Ctrl + Click сработал!';
      }
    },

    // Задача №3
    handleMouseClick(event) {
      event.preventDefault(); // чтобы избежать перехода по ссылке
      if (event.button === 0) {
        this.mouseClickText = 'left';
      } else if (event.button === 1) {
        this.mouseClickText = 'middle';
      } else if (event.button === 2) {
        this.mouseClickText = 'right';
      }
    },
  },
};
</script>

<template>
  <div style="padding: 20px; font-family: sans-serif">
    <!-- Задача №1 -->
    <section style="margin-bottom: 40px;">
      <h2>№1</h2>
      <p>Введите текст и нажмите Enter:</p>
      <input
        type="text"
        v-model="inputText"
        @keydown="handleKeyPress"
        placeholder="Введите что-нибудь"
      />
      <p>{{ submittedText }}</p>
    </section>

    <!-- Задача №2 -->
    <section style="margin-bottom: 40px;">
      <h2>№2</h2>
      <p>
        <a href="#" @click.prevent="handleCtrlClick">Кликни по этой ссылке с зажатым Ctrl</a>
      </p>
      <p>{{ ctrlClickText }}</p>
    </section>

    <!-- Задача №3 -->
    <section>
      <h2>№3</h2>
      <p>
        <a href="#"
           @mousedown="handleMouseClick"
           @contextmenu.prevent
        >Кликни по этой ссылке разными кнопками мыши</a>
      </p>
      <p>{{ mouseClickText }}</p>
    </section>
  </div>
</template>

<style scoped>
a {
  color: #007acc;
  cursor: pointer;
  text-decoration: underline;
}
input {
  padding: 6px;
  margin-top: 5px;
}
</style>
