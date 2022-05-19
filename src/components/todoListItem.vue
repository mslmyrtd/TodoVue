<template>
  <div class="flex justify-between items-center even:bg-slate-600 px-2 p-1">
    <label for="`todo_${todo.id}_completed`">
      <input
        type="checkbox"
        v-model="todo.completed"
        :id="`todo_${todo.id}_completed`"
        class="mr-2"
      />
      <span class="text-lg">{{ todo.title }}</span>
    </label>

    <button
      @click="deleteItem"
      class="bg-red-400 px-2 py-1 rounded-md active:bg-red-600"
    >
      Delete
    </button>
  </div>
</template>
<script>
export default {
  props: {
    todo: Object,
  },
  setup(props, { emit }) {
    const deleteItem = () => {
      emit("delete-event", props.todo);
    };
    return {
      deleteItem,
    };
  },
};
</script>
