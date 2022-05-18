<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
import HelloWorld from "./components/HelloWorld.vue";
</script>

<template>
  <div class="w-screen h-screen bg-gray-400 pt-10">
    <div class="bg-gray-700 rounded-md shadow-md text-white w-1/3 mx-auto p-3">
      <h3 class="text-center text-2xl">Task Tracker</h3>
      <hr />
      <section class="mt-5">
        <input
          type="text"
          placeholder="Add Task"
          class="w-full p-2 rounded-lg bg-gray-600 border-2 border-gray-400 outline-none"
        />
      </section>
      <section class="mt-4">
        <div
          class="flex justify-between items-center even:bg-slate-600 px-2 p-1"
        >
          <label for="completed">
            <input type="checkbox" id="completed" class="mr-2" />
            <span class="text-lg">Todo1</span>
          </label>
          <button class="bg-red-400 px-2 py-1 rounded-md active:bg-red-600">
            Delete
          </button>
        </div>
        <div class="flex justify-around">
          <small class="text-green-400">Done</small>
          <small class="text-red-400">Undone</small>
        </div>
      </section>
    </div>
  </div>
</template>

<style></style>
