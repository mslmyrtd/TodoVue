<template>
  <div class="flex justify-around" v-if="todoLength">
    <small class="text-green-400 underline">Done : {{ completed }}</small>
    <small class="text-red-400 underline">Undone : {{ unCompleted }} </small>
  </div>
</template>
<script>
import { computed } from "vue";
export default {
  props: {
    todoList: Array,
    todoLength: Number,
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
