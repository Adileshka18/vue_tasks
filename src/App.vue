<template>
  <div>
    <!-- Задание 1 -->
    <label>
      <input type="radio" value="English" v-model="nativeLanguage"> English
    </label>
    <label>
      <input type="radio" value="Spanish" v-model="nativeLanguage"> Spanish
    </label>
    <label>
      <input type="radio" value="French" v-model="nativeLanguage"> French
    </label>

    <p>Выбранный язык: {{ nativeLanguage }}</p>

    <!-- Задание 2 -->
    <div>
      <p v-if="nativeLanguage === 'English'">Hello!</p>
      <p v-if="nativeLanguage === 'Spanish'">¡Hola!</p>
      <p v-if="nativeLanguage === 'French'">Bonjour!</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      nativeLanguage: '',
    };
  },
};
</script>