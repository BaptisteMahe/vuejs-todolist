<template>
  <div class="todo">
    {{ todo }}
  </div>
</template>

<script>
export default {
  name: "Todo",
  props: {
    todo: String,
  },
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
}

.todo:hover {
  background-color: rgb(44, 62, 80, 0.1);
}
</style>