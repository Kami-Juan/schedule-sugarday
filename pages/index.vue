<template>
  <div class="container">
    <div class="schedule-container">
      <div class="schedule-header">
        <h1 class="schedule-title">
          SUGARDAY(?)
        </h1>
        <Counter />
      </div>
      <div class="livestream-container">
        <div
          v-for="(livestream, i) in livestreams"
          :key="i"
          class="schedule-column"
        >
          <LivestreamItem
            :content="livestream.content"
            :url="livestream.url"
            :date="livestream.date"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Counter from '~/components/ui/counter/Counter'
import LivestreamItem from '~/components/ui/livestream/LivestreamItem'

export default {
  components: { Counter, LivestreamItem },
  data() {
    return {
      livestreams: [
        {
          url: 'https://randomuser.me/api/portraits/men/75.jpg',
          content: 'Programming your business for change',
          date: '14:00 PM'
        },
        {
          url: 'https://randomuser.me/api/portraits/men/75.jpg',
          content: 'Programming your business for change',
          date: '14:00 PM'
        },
        {
          url: 'https://randomuser.me/api/portraits/men/75.jpg',
          content: 'Programming your business for change',
          date: '14:00 PM'
        },
        {
          url: 'https://randomuser.me/api/portraits/men/75.jpg',
          content: 'Programming your business for change',
          date: '14:00 PM'
        }
      ]
    }
  }
}
</script>

<style lang="postcss">
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  min-width: 100vw;
}

.schedule-container {
  @apply flex flex-col;
  background-color: #ffaa00;
  background-image: url('../assets/images/Liquid-Cheese.svg');
  background-attachment: fixed;
  background-size: cover;
  height: 100%;
  padding: 3rem 0;
  width: calc(100vw - 12rem);
  box-shadow: -6px 10px 0px 2px #f8b51f, -12px 16px 0px 2px #f0bf3e;
  border-radius: 10px 0px 10px 0;
}

.schedule-header {
  @apply flex justify-between;
}

.schedule-column {
  height: 25%;
  width: 100%;
}

.livestream-container {
  @apply flex flex-col;
  flex: 1;
}

.schedule-title {
  font-family: 'Lato', sans-serif;
  display: block;
  font-weight: 500;
  font-size: 4rem;
  color: black;
  letter-spacing: 1px;
  padding-left: 0.8rem;
}
</style>
