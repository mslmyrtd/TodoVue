<script>
import todoList from "./components/todoList.vue";
import { ref } from "vue";
import addTodo from "./components/addTodo.vue";
export default {
  components: {
    addTodo,
    todoList,
  },
  setup() {
    const todoList = ref([]);
    return { todoList };
  },
};
</script>

<template>
  <div class="w-screen h-screen bg-gray-400 pt-10">
    <div class="bg-gray-700 rounded-md shadow-md text-white w-1/3 mx-auto p-3">
      <h3 class="text-center text-2xl">Task Tracker</h3>
      <hr />
      <addTodo />
      <todoList :todoList="todoList" />
    </div>
  </div>
</template>

<style></style>
