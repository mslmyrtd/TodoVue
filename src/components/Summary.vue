<template>
  <div class="flex justify-around">
    <small class="text-green-400">Done{{ completed }}</small>
    <small class="text-red-400">Undone {{ unCompleted }} </small>
  </div>
</template>
<script>
import { computed } from "vue";
export default {
  props: {
    todoList: Array,
  },
  setup(props) {
    const completed = computed(
      () => props.todoList.filter((i) => i.completed).length
    );
    const unCompleted = computed(
      () => props.todoList.filter((i) => !i.completed).length
    );
    return {
      completed,
      unCompleted,
    };
  },
};
</script>
