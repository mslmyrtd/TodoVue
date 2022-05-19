<template>
  <section class="mt-4">
    <TodoListItem
      @delete-event="$emit('delete-event', $event)"
      v-for="todoItem in todoList"
      :key="todoItem.id"
      :todo="todoItem"
    />
    <hr />
    <p v-if="todoLength == 0" class="text-center text-sm">
      There is no todo to do
    </p>
    <small v-else>Number of todo : {{ todoLength }} </small>
    <Summary :todoList="todoList" :todoLength="todoLength" />
  </section>
</template>
<script>
import TodoListItem from "./todoListItem.vue";
import Summary from "./Summary.vue";
import { computed } from "vue";
export default {
  components: {
    TodoListItem,
    Summary,
  },
  props: {
    todoList: Array,
  },
  setup(props) {
    const todoLength = computed(() => props.todoList.length);
    return { todoLength };
  },
};
</script>
