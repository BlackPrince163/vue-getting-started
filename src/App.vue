<template>
  <h1>Hello world</h1>
  <a href="http://yandex.ru">Yandex</a>
  <br>
  <p><span>Счетчик: <b>{{ count }}</b></span></p>
  <input type="number" placeholder="Счетчик">
  <button>Увеличить счетчик</button>
</template>

<script>
  export default {
    data() {
      return {
        count: 0
      };
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
