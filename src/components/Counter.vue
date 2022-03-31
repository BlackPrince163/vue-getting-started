<template>
    <div class="counter">
        <input type="number" placeholder="Счетчик" v-model="count">
        <button @click="clickHandler">Увеличить счетчик</button>
    </div>
</template>

<script>
export default {
    name: "Counter",
    data() {
        return {
            count: 0
        };
    },
    methods: {
        clickHandler() {
            this.count++;
        }
    },
    watch: {
        count(newValue) {
            this.$emit("updateCount", newValue);
        }
    }
}
</script>

<style scoped>
    .counter {
        border: 1px solid blue;
        padding: 10px;
    }
</style>