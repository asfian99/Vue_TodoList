<template>
  <div id="app">
    <Todos v-bind:todosData="todosData" />
  </div>
</template>

<script>
import Todos from "./components/Todos";

export default {
  name: "App",
  components: {
    Todos,
  },
  data() {
    return {
      todosData: [
        {
          id: 1,
          title: "todo one",
          completed: false,
        },
        {
          id: 2,
          title: "todo two",
          completed: false,
        },
        {
          id: 3,
          title: "todo three",
          completed: false,
        },
      ],
    };
  },
};
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
body {
  font-family: Arial, Helvetica, sans-serif;
  line-height: 1.4;
}
</style>
