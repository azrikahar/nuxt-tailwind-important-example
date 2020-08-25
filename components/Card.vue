<template>
  <div class="card">
    <slot></slot>
    <div class="mt-2 font-semibold">{{ classList }}</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      classList: [],
    }
  },
  mounted() {
    this.classList = Array.from(this.$el.classList)
  },
}
</script>

<style scoped>
.card {
  @apply p-4 rounded border;
}
.card-gray {
  @apply bg-gray-200 text-gray-800 border-gray-300;
}
.card-blue {
  @apply bg-blue-200 text-blue-800 border-blue-300;
}
</style>
