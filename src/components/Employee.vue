<template>
  <tr>
    <td>{{ name }}</td>
    <td>{{ surname }}</td>
    <td>{{ age }}</td>
  </tr>
</template>

<script>
export default {
  props: {
    name: String,
    surname: String,
    age: Number
  }
};
</script>
