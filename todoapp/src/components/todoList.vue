<template>
  <section class="mt-4">
    <TodoListItem />
    <Summary />
  </section>
</template>
<script>
import todoListItem from "./todoListItem.vue";
import Summary from "./Summary.vue";
export default {
  components: {
    todoListItem,
    Summary,
  },
};
</script>
