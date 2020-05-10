<template>
  <div class="item-container">
    <LivestreamUser :url="url" />
    <LivestreamContent :content="content" />
    <LivestreamDate :date="date" />
  </div>
</template>
<script>
import LivestreamUser from '~/components/ui/livestream/LivestreamUser'
import LivestreamContent from '~/components/ui/livestream/LivestreamContent'
import LivestreamDate from '~/components/ui/livestream/LivestreamDate'

export default {
  components: { LivestreamUser, LivestreamContent, LivestreamDate },
  props: {
    url: {
      type: String,
      required: true
    },
    content: {
      type: String,
      required: true
    },
    date: {
      type: String,
      required: true
    }
  }
}
</script>
<style lang="postcss">
.item-container {
  @apply flex items-center;
  height: 100%;
  padding: 0 2rem;
  margin: 0.2rem;
}
</style>
