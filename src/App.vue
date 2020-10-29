<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <Todo todo="Faire les courses" />
  <Todo todo="Faire le tuto Vue" />
  <Todo todo="Faire une liste de Todo" />
</template>

<script>
import Todo from "./components/Todo.vue";

export default {
  name: "App",
  components: {
    Todo,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin: 60px 25% 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  font-size: 1.5em;
}
</style>
