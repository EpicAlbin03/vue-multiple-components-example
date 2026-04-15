<template>
  <div class="stars">
    <span v-for="n in 5" :key="n" :class="{ filled: n <= rating }">
      ★
    </span>
  </div>
</template>

<script>
export default {
  props: {
    rating: {
      type: Number,
      required: true
    }
  }
}
</script>

<style scoped>
.stars {
  font-size: 18px;
  letter-spacing: 2px;
}

.stars span {
  color: #d1d5db;
}

.stars span.filled {
  color: #f59e0b;
}
</style>
