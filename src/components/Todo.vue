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
</style>