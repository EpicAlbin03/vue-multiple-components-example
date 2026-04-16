<script>
import TagBadge from "./TagBadge.vue"

export default {
  components: {
    TagBadge,
  },

  props: {
    rating: {
      type: Number,
      required: true,
    },
  },
}
</script>

<template>
  <div class="stars">
    <TagBadge :rating="rating" label="★" />
  </div>
</template>

<style scoped>
.stars {
  font-size: 18px;
  letter-spacing: 2px;
}
</style>
