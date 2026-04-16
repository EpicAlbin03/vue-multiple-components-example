<script>
export default {
  props: {
    title: {
      type: String,
      required: true,
    },
    recipeCount: {
      type: Number,
      required: true,
    },
  },
}
</script>

<template>
  <header>
    <h1>{{ title }}</h1>
    <p>{{ recipeCount }} recipes</p>
  </header>
</template>

<style>
header {
  margin-bottom: 30px;
}

header h1 {
  color: #0f172a;
  margin-bottom: 4px;
}

header p {
  color: #6b7280;
}
</style>
