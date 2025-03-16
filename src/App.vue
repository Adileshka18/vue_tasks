<script>
export default {
    data() {
        return {
            text: 'xxx',
        };
    },
    methods: {
        changeToYYY() {
            this.text = 'yyy';
        },
        changeToZZZ() {
            this.text = 'zzz';
        }
    }
}
</script>

<template>
    {{ text }}
    <button @click="changeToYYY">Изменить на yyy</button>
    <button @click="changeToZZZ">Изменить на zzz</button>
</template>
