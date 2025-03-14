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
    <button @click="show">Показать дату</button>
</template>