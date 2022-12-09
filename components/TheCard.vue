<script setup>
  defineProps({
    title:{
      type: String,
      default: "Title",
    },
    Instruction:{
      type: String,
      default: "Instruction",
    },
    src: String,
    alt: String
  });
</script>

<template>
  <div class="p-20 w-full">
    <div class="bg-white rounded-lg shadow-lg">
      <img :src="src" :alt="alt" class="rounded-t-lg"/>
      <div class="p-6">
        <h2 class="font-bold mb-2 text-2xl text-purple-800">{{title}}</h2>
        <p class="text-purple-700 mb-2">{{Instruction}}</p>
        <a href="#" class="text-purple-600 hover:text-purple-500 underline text-sm">Read More 👉</a>
      </div>
    </div>
  </div>
</template>
