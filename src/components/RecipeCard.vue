<script>
import RatingStars from "./RatingStars.vue"

export default {
  components: {
    RatingStars,
  },

  props: {
    recipe: {
      type: Object,
      required: true,
    },
  },
}
</script>

<template>
  <div class="card">
    <div class="card-header">
      <h2>{{ recipe.name }}</h2>
      <span class="time">{{ recipe.time }} min</span>
    </div>
    <p class="description">{{ recipe.description }}</p>

    <RatingStars :rating="recipe.rating" />

    <div class="tags">
      <span v-for="tag in recipe.tags" :key="tag" class="tag">
        {{ tag }}
      </span>
    </div>
  </div>
</template>

<style scoped>
.card {
  background: white;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.06);
}

.card-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 8px;
}

.card-header h2 {
  font-size: 18px;
  color: #0f172a;
}

.time {
  background-color: #e2e8f0;
  color: #475569;
  padding: 3px 10px;
  border-radius: 12px;
  font-size: 12px;
}

.description {
  color: #6b7280;
  font-size: 14px;
  margin-bottom: 10px;
}

.tags {
  display: flex;
  gap: 6px;
  margin-top: 10px;
}

.tag {
  background-color: #ede9fe;
  color: #6d28d9;
  padding: 2px 10px;
  border-radius: 12px;
  font-size: 12px;
}
</style>
