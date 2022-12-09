<script setup>
  const { data: meals } = await useFetch('https://www.themealdb.com/api/json/v1/1/random.php')
</script>

<template>
  <TheHeader pageName="Recipes"/>
  <div class="grid grid-cols-3">
    <TheCard v-for="meal in meals.meals"
    :title="meal.strMeal"
    :src="meal.strMealThumb"
    :alt="meal.strMeal"
    :Instruction="meal.strInstructions"/>
  </div>
</template>