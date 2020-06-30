<template>
  <div>
    <div v-for="todo in todosData" :key="todo.id">
      <h3>{{ todo.title }}</h3>
    </div>
  </div>
</template>

<script>
export default {
  name: "Todos",
  props: ["todosData"],
};
</script>

<style scoped></style>
