<template>
  <div class="content-container">
    {{ content }}
  </div>
</template>
<script>
export default {
  props: {
    content: {
      type: String,
      required: true
    }
  }
}
</script>
<style lang="postcss">
.content-container {
  @apply flex items-center;
  width: 70%;
  height: 100%;
  color: black;
  padding: 0.4rem 0 1rem 2rem;
  font-size: 2.4rem;
  font-weight: 400;
}
</style>
