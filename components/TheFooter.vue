<script setup>
  defineProps({
    footer:{
      type: String,
      default: "© 2022 Copyright: Dohyeong Kim",
    },
  });
</script>

<template>
    <div class="position: fixed bottom-0 left-0 text-center p-4 w-full h-16 " style="background-color: white">
      <footer>{{footer}}</footer>
    </div>
</template>