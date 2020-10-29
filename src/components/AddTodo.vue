<template>
  <input
    class="todo-input"
    v-on:keyup.enter="onSubmit"
    v-model="todo"
    placeholder="Ajoutez un todo !"
  />
</template>

<script>
export default {
  name: "AddTodo",
  methods: {
    onSubmit: function () {
      console.log(this.todo);
    },
  },
  data() {
    return {
      todo: "",
    };
  },
};
</script>

<style scoped>
.todo-input {
  width: 50%;
  font-size: 1.5em;
  margin: 20px;
  color: #2c3e50;
}
</style>