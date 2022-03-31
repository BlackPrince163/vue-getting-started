<template>
    <h1>Hello world</h1>
    <a href="http://yandex.ru">Yandex</a>
    <br>
    <p><span>Счетчик: <b>{{ count }}</b></span></p>
    <Counter @updateCount="updateCountHandler" />
</template>

<script>
    import Counter from "@/components/Counter.vue";

    export default {
        components: {Counter},
        data() {
            return {
                count: 0
            };
        },
        methods: {
            updateCountHandler(count) {
                this.count = count
            }
        }
    };
</script>

<style>
    h1 {
        color: blue;
    }

    a {
        background: black;
        color: white;
    }
</style>
