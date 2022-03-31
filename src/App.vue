<template>
    <h1>Hello world</h1>
    <a href="http://yandex.ru">Yandex</a>
    <br>
    <p><span>Счетчик: <b>{{ count }}</b></span></p>
    <Counter />
</template>

<script>
    import Counter from "@/components/Counter.vue";

    export default {
        components: {Counter},
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
