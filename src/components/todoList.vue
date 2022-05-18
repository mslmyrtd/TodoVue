<template>
  <section class="mt-4">
    <TodoListItem
      @delete-event="$emit('delete-even', $event)"
      v-for="todoItem in todoList"
      :key="todoItem.id"
      :todo="todoItem"
    />
    <small>Number of items {{ todoLength }} </small>
    <Summary />
  </section>
</template>
<script>
import todoListItem from "./todoListItem.vue";
import Summary from "./Summary.vue";
import { computed } from "vue";
export default {
  components: {
    todoListItem,
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
