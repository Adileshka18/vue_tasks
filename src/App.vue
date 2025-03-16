<script>
export default {
    data() {
        
    },
    methods: {
        show() {
            let day = this.getDayOfWeek(new Date().getDay());
            alert(day);
        },
        getDayOfWeek(num) {
            const days = ["Воскресенье", "Понедельник", "Вторник", "Среда", "Четверг", "Пятница", "Суббота"];
            return days[num] || "Некорректное число";
        }
    }
}
</script>

<template>
    <button @click="show">Показать день недели</button>
</template>
