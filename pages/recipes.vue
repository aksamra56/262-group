<script setup>
  const { data: meals } = await useFetch('https://www.themealdb.com/api/json/v1/1/filter.php?c=Seafood')
</script>

<template>
  <TheHeader pageName="Recipes"/>
  <div class="flex flex-wrap">
    <TheCard v-for="meal in meals.meals"
    :link="`/details/${meal.idMeal}`"
    :title="meal.strMeal"
    :src="meal.strMealThumb"
    :alt="meal.strMeal"
    />
  </div>
</template>