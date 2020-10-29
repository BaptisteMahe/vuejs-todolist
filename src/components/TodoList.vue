<template>
  <div class="todo-list">
    <Todo
      v-for="(todo, index) in todos"
      :key="todo"
      v-bind:todo="todo"
      v-bind:index="index"
      v-on:delete-todo="deleteThisTodo"
    />
  </div>
</template>

<script>
import Todo from "./Todo.vue";

export default {
  name: "TodoList",
  components: {
    Todo,
  },
  methods: {
    deleteThisTodo: function (todoIndex) {
      console.log(todoIndex);
      this.todos.splice(todoIndex, 1);
    }
  },
  data() {
    return {
      todos: [
        "Faire les courses",
        "Faire le tuto Vue",
        "Faire une liste de Todo",
      ],
    };
  }
};
</script>

<style scoped>
.todo-list {
  width: 100%;
}
</style>