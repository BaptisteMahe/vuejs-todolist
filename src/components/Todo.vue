<template>
  <div class="todo">
    <p>{{ todo }}</p>
    <button v-on:click="$emit('delete-todo', index)">delete</button>
  </div>
</template>

<script>
export default {
  name: "Todo",
  props: {
    todo: String,
    index: Number,
  }, 
  emits: ["delete-todo"]
};
</script>

<style scoped>
.todo {
  padding: 5px;
  margin: 5px;
  width: 100%;
  border-radius: 10px;
  color: #2c3e50;
  border-style: solid;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.todo:hover {
  background-color: rgb(44, 62, 80, 0.1);
}

button {
  width: 70px;
  height: 30px;
  border-radius: 15px;
  border-color: rgb(182, 80, 80);
  border-width: 3px;
  background-color: rgb(255, 202, 202);
}

p {
  margin: 5px;
}
</style>