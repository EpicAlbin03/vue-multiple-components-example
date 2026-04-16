<script>
export default {
  props: {
    label: {
      type: String,
      required: true,
    },
    rating: {
      type: Number,
      required: true,
    },
  },
}
</script>

<template>
  <span v-for="n in 5" :key="n" :class="{ filled: n <= rating }">{{ label }}</span>
</template>

<style scoped>
span {
  color: #d1d5db;
}

span.filled {
  color: #f59e0b;
}
</style>
