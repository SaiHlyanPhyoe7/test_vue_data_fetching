<template>
  <div class="">
    <button
      class="border z-50 mx-auto relative bg-indigo-400 text-white px-5 hover:text-yellow-400 duration-500 flex justify-center items-center rounded-full py-3 mt-20"
    >
      Hover Me
      <div
        class="hover:border absolute z-20 inset-0 px-2 py-3 rounded-xl hover:scale-x-[3] hover:scale-y-[1.8] hover:opacity-0 hover:duration-300 hover:ring hover:ring-yellow-400 hover:border-yellow-500 text-white"
      ></div>
    </button>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped></style>
