<template>
  <div>
    <!-- Задание 1 -->
    <label>
      <input type="checkbox" value="English" v-model="languages"> English
    </label>
    <label>
      <input type="checkbox" value="Spanish" v-model="languages"> Spanish
    </label>
    <label>
      <input type="checkbox" value="French" v-model="languages"> French
    </label>
    <label>
      <input type="checkbox" value="German" v-model="languages"> German
    </label>
    <label>
      <input type="checkbox" value="Russian" v-model="languages"> Russian
    </label>

    <!-- Задание 2 -->
    <ul>
      <li v-for="(language, index) in languages" :key="index">{{ language }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      languages: [],
    };
  },
};
</script>