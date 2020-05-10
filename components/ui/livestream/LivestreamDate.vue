<template>
  <div class="date-container">
    {{ date }}
  </div>
</template>
<script>
export default {
  props: {
    date: {
      type: String,
      required: true
    }
  }
}
</script>
<style lang="postcss">
.date-container {
  @apply flex items-center;
  width: 15%;
  height: 100%;
  font-size: 2rem;
  font-weight: 400;
}
</style>
