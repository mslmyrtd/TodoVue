<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
import HelloWorld from "./components/HelloWorld.vue";
</script>

<template>
  <div class="w-screen h-screen bg-gray-400 pt-10">
    <div class="bg-gray-700 rounded-md shadow-md text-white w-1/3 mx-auto p-3">
      <h3 class="text-center text-2xl">Task Tracker</h3>
      <section class="mt-4">
        <div class="flex justify-between items-center bg-slate-600 px-2 p-1">
          <label for="completed">
            <input type="checkbox" id="completed" />
            Todo1
          </label>
          <button class="bg-red-400 px-2 py-1 rounded-md active:bg-red-600">
            Sil
          </button>
        </div>
      </section>
    </div>
  </div>
</template>

<style></style>
