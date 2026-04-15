<template>
  <div class="main-app">
    <header>
      <h1>My Recipe Book</h1>
      <p>{{ recipes.length }} recipes</p>
    </header>

    <main>
      <RecipeCard
        v-for="recipe in recipes"
        :key="recipe.id"
        :recipe="recipe"
      />
    </main>
  </div>
</template>

<script>
import RecipeCard from './components/RecipeCard.vue'

export default {
  components: {
    RecipeCard
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
          tags: ["Italian", "Pasta", "Quick"]
        },
        {
          id: 2,
          name: "Chicken Tikka Masala",
          description: "Creamy spiced curry with tender chicken pieces.",
          time: 45,
          rating: 4,
          tags: ["Indian", "Curry", "Spicy"]
        },
        {
          id: 3,
          name: "Caesar Salad",
          description: "Crunchy romaine with parmesan, croutons, and creamy dressing.",
          time: 15,
          rating: 3,
          tags: ["Salad", "Quick", "Healthy"]
        }
      ]
    }
  }
}
</script>

<style>
* { margin: 0; padding: 0; box-sizing: border-box; }

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

main {
  display: flex;
  flex-direction: column;
  gap: 15px;
}
</style>
