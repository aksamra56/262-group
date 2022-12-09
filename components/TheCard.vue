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
  <div class="p-20 flex justify-center">
    <div class="bg-white rounded-lg shadow-lg">
      <img :src="src" :alt="alt" class="rounded-t-lg"/>
      <div class="p-6">
        <h2 class="font-bold mb-2 text-2xl text-center">{{title}}</h2>
        <div class="mt-5">
          <div class="w-full">
            <div class="flex-1 h-full w-44">
              <div class="flex w-full bg-orange-400 shadow rounded-xl hover:scale-105">
                <p class="m-auto text-xl font-semibold text-center py-2">Show me!</p>
                <div class="">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 mt-3 mr-3" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3" />
                  </svg>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
