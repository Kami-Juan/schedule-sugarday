<template>
  <div class="user-container">
    <figure class="">
      <img :src="url" alt="" />
    </figure>
  </div>
</template>
<script>
export default {
  props: {
    url: {
      type: String,
      required: true
    }
  }
}
</script>
<style lang="postcss">
.user-container {
  width: 8%;
  height: 100%;
  @apply flex items-center;
}

.user-container > figure {
}
</style>
