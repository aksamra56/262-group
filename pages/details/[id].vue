<script setup>
  const { id } = useRoute().params; 
  const uri = `https://www.themealdb.com/api/json/v1/1/lookup.php?i=${id}`;

  const { data: food } = await useFetch(uri, { key: id });
</script>

<template>
  <Details :food="food" />
</template>