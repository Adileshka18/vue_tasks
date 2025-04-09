<template>
  <div>
    <!-- Задание 1 -->
    <ul>
      <li v-for="(item, index) in hrefs" :key="index">
        <a :href="item.href">{{ item.text }}</a>
      </li>
    </ul>

    <!-- Задание 2 -->
    <table>
      <tr v-for="(product, index) in products" :key="index">
        <td>{{ product.name }}</td>
        <td>{{ product.price }}</td>
        <td>{{ product.quantity }}</td>
      </tr>
    </table>
  </div>
</template>

<script>
export default {
  data() {
    return {
      hrefs: [
        { href: '1.html', text: 'text1' },
        { href: '2.html', text: 'text2' },
        { href: '3.html', text: 'text3' }
      ],
      products: [
        { name: 'product1', price: 100, quantity: 5 },
        { name: 'product2', price: 200, quantity: 4 },
        { name: 'product3', price: 300, quantity: 3 }
      ]
    };
  }
}
</script>

<style scoped>
ul {
  list-style-type: none;
}

li {
  margin: 5px 0;
}

table {
  width: 100%;
  border-collapse: collapse;
}

td {
  padding: 8px;
  border: 1px solid #ccc;
}
</style>