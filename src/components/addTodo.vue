<script>
export default {
  props: {
    AddTodo: Function,
  },
  setup(props) {
    const newItem = (event) => {
      props.AddTodo(event.target.value);
      event.target.value = "";
    };
    return {
      newItem,
    };
  },
};
</script>

<template>
  <section class="mt-5">
    <span>Todo</span>
    <input
      @keydown.enter="newItem"
      type="text"
      placeholder="Add Task"
      class="w-full p-1 rounded-lg bg-gray-600 border-2 border-gray-400 outline-none"
    />
    <!-- <span class="mt-5">Date</span>
    <input
      type="date"
      placeholder="Date"
      class="w-full p-1 rounded-lg bg-gray-600 border-2 border-gray-400 outline-none"
    /> -->
  </section>
</template>

<style scoped></style>
