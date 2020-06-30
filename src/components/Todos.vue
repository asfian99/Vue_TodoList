<template>
  <div>
    <div v-for="todo in todosData" :key="todo.id">
      <TodoItem v-bind:todo="todo" />
    </div>
  </div>
</template>

<script>
import TodoItem from "./TodoItem";
export default {
  name: "Todos",
  components: {
    TodoItem,
  },
  props: ["todosData"],
};
</script>

<style scoped></style>
