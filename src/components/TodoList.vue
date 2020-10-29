<template>
  <div class="todo-list">
    <Todo v-for="todo in todos" :key="todo" v-bind:todo="todo" />
  </div>
</template>

<script>
import Todo from "./Todo.vue";

export default {
  name: "TodoList",
  components: {
    Todo,
  },
  props: {
    todos: Array
  }
};
</script>

<style scoped>
.todo-list {
  width: 100%;
}
</style>