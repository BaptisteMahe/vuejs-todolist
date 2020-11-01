<template>
  <div class="todo-list">
    <div v-if="todos.length > 0">
      <Todo
        v-for="(todo, index) in todos"
        :key="todo"
        v-bind:todo="todo"
        v-bind:index="index"
        v-on:delete-todo="deleteThisTodo"
      />
    </div>
    <div v-else class="todo-list-empty">
      Vous n'avez plus rien à faire, bien joué !
    </div>
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
    },
  },
  data() {
    return {
      todos: [],
    };
  },
};
</script>

<style scoped>
.todo-list {
  width: 100%;
}
.todo-list-empty {
  text-align: center;
  color: green;
}
</style>