<script>
export default {
    data() {
        return {
            num1: 1,
            num2: 2,
        };
    },
    methods: {
        show() {
            alert(this.num1 + this.num2);
        }
    }
}
</script>

<template>
    <button @click="show">Показать сумму</button>
</template>