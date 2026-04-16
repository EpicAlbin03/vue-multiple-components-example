<script>
import RecipeCard from "./components/RecipeCard.vue"
import AppHeader from "./components/AppHeader.vue"

export default {
  components: {
    RecipeCard,
    AppHeader,
  },

  data() {
    return {
      recipes: [
        {
          id: 1,
          name: "Spaghetti Carbonara",
          description: "Classic Italian pasta with eggs, cheese, and pancetta.",
          time: 25,
          rating: 5,
          tags: ["Italian", "Pasta", "Quick"],
        },
        {
          id: 2,
          name: "Chicken Tikka Masala",
          description: "Creamy spiced curry with tender chicken pieces.",
          time: 45,
          rating: 4,
          tags: ["Indian", "Curry", "Spicy"],
        },
        {
          id: 3,
          name: "Caesar Salad",
          description: "Crunchy romaine with parmesan, croutons, and creamy dressing.",
          time: 15,
          rating: 3,
          tags: ["Salad", "Quick", "Healthy"],
        },
      ],
    }
  },
}
</script>

<template>
  <div class="main-app">
    <AppHeader title="My Recipe Book" :recipeCount="recipes.length" />

    <main>
      <RecipeCard v-for="recipe in recipes" :key="recipe.id" :recipe="recipe" />
    </main>
  </div>
</template>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Arial, sans-serif;
  background-color: #f5f7fa;
  color: #333;
  line-height: 1.6;
}

.main-app {
  max-width: 800px;
  margin: 0 auto;
  padding: 30px;
}

main {
  display: flex;
  flex-direction: column;
  gap: 15px;
}
</style>
