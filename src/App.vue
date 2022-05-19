<template>
  <div class="w-screen h-screen bg-gray-400 pt-10">
    <div class="bg-gray-700 rounded-md shadow-md text-white w-1/3 mx-auto p-3">
      <h3 class="text-center text-2xl">Task Tracker</h3>
      <hr />
      <AddTodo :AddTodo="AddTodo" />
      <TodoList :todoList="todoList" @delete-event="deleteItem" />
    </div>
  </div>
</template>

<script>
import TodoList from "./components/todoList.vue";
import { ref } from "vue";
import AddTodo from "./components/addTodo.vue";
export default {
  components: {
    AddTodo,
    TodoList,
  },
  setup() {
    const todoList = ref([]);
    const AddTodo = (todoText) => {
      console.log(todoText);
      todoList.value.push({
        id: new Date().getTime(),
        title: todoText,
      });
    };
    const deleteItem = (todo) => {
      todoList.value = todoList.value.filter((t) => t.id != todo.id);
    };
    return { todoList, AddTodo, deleteItem };
  },
};
</script>

<style></style>
