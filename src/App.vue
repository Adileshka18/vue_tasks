<script>
export default {
    methods: {
        show() {
            alert(new Date().toLocaleDateString());
        }
    }
}
</script>

<template>
    <button @click="show">Показать дату при нажатии</button>
    <button @mouseover="show">Показать дату при наведении</button>
</template>