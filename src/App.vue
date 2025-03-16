<script>
export default {
    methods: {
        showSquare(num) {
            alert(num * num);
        }
    }
}
</script>

<template>
    <button @click="showSquare(2)">Показать квадрат 2</button>
    <button @click="showSquare(3)">Показать квадрат 3</button>
</template>
