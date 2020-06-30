<template>
  <div id="app">
    <Header />
    <AddTodo v-on:add-todo="addTodo" />
    <Todos v-bind:todosData="todosData" v-on:del-todo="deleteTodo" />
  </div>
</template>

<script>
import Header from "./components/layout/Header";
import Todos from "./components/Todos";
import AddTodo from "./components/AddTodo";

export default {
  name: "App",
  components: {
    Header,
    Todos,
    AddTodo,
  },
  data() {
    return {
      todosData: [
        {
          id: 1,
          title: "makan pagi",
          completed: false,
        },
        {
          id: 2,
          title: "makan siang",
          completed: false,
        },
        {
          id: 3,
          title: "makan malam",
          completed: false,
        },
      ],
    };
  },
  methods: {
    deleteTodo(id) {
      this.todosData = this.todosData.filter((todo) => todo.id !== id);
    },
    addTodo(newTodo) {
      this.todosData = [...this.todosData, newTodo];
    },
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
.btn {
  display: inline-block;
  border: none;
  background: #555;
  color: #fff;
  padding: 7px 20px;
  cursor: pointer;
}
.btn:hover {
  background: #666;
}
</style>
