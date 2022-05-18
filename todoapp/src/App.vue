<script>
import todoListItem from "./components/todoListItem.vue";
import todoList from "./components/todoList.vue";
import Summary from "./components/Summary.vue";
import addTodo from "./components/addTodo.vue";
export default {
  components: {
    todoListItem,
    Summary,
    addTodo,
    todoList,
  },
};
</script>

<template>
  <div class="w-screen h-screen bg-gray-400 pt-10">
    <div class="bg-gray-700 rounded-md shadow-md text-white w-1/3 mx-auto p-3">
      <h3 class="text-center text-2xl">Task Tracker</h3>
      <hr />
      <addTodo />
      <todoList />
    </div>
  </div>
</template>

<style></style>
