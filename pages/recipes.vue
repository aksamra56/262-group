<script setup>
  const { data: meals } = await useFetch('www.themealdb.com/api/json/v1/1/random.php')
</script>

<template>
  <div class="grid grid-cols-3">
    <TheCard v-for="meal in meals"
    :title="meal.strMeal"
    :image="meal.strMealThumb"
    :Instruction="meal.strInstructions"/>
  </div>
</template>