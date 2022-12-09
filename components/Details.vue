<script setup>
  const{food} = defineProps(["food"]);
</script>

<template>
  <div v-for="details in food.meals">
    <img :src= "details.strMealThumb" width="400" height="400" class="flex justify-center mx-auto m-10"/>
    <h1 class="text-center text-3xl pb-5">{{details.strMeal}}</h1>
    <p class="mx-auto max-w-2xl">{{details.strInstructions}}</p>
  </div>
</template>