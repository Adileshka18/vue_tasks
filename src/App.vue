<script>
export default {
    data() {
        return {
            cost: 100,
            amount: 2,
        };
    }, 

    computed: {
        price() {
            return this.cost * this.amount;
        }
    },

    methods: {
        changeCost() {
            this.cost += 50;
        }
    }
}
</script>

<template>
    <p>Цена: {{ cost }}</p>
    <p>Количество: {{ amount }}</p>
    <p>Полная стоимость: {{ price }}</p>
    <button @click="changeCost">Изменить цену</button>
</template>
