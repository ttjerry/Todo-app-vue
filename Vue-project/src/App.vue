<script setup>
import todoHeader from './components/todo-header.vue';
import todos from './components/todos.vue';

</script>
<template>
  <header>
    <todoHeader />
    <todos />
  </header>
</template>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Rubik:ital,wght@0,300;1,300&display=swap');

* {
  font-family: "Rubik", sans-serif;
  margin: 0;
  background-color: hsl(235, 21%, 11%);
  padding: 0;
}

</style>
