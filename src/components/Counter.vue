<template>
    <div class="counter">
        <input type="number" placeholder="Счетчик" v-model="count">
        <button @click="clickHandler">Увеличить счетчик</button>
    </div>
</template>

<script>
export default {
    name: "Counter",
    props: {
        initialValue: {
            type: Number,
            default: 0
        }
    },
    data() {
        return {
            count: this.initialValue
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