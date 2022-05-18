<template>
  <div class="flex justify-between items-center even:bg-slate-600 px-2 p-1">
    <label for="completed">
      <input
        type="checkbox"
        v-model="todo.completed"
        id="completed"
        class="mr-2"
      />
      <span class="text-lg">{{ todo.tile }}</span>
      <span class="text-lg">{{ todo.date }}</span>
    </label>
    <button class="bg-red-400 px-2 py-1 rounded-md active:bg-red-600">
      Delete
    </button>
  </div>
</template>
<script>
export default {
  props: {
    todo: Object,
  },
  setup() {},
};
</script>
