<template>
  <div>
    <nav-bar />
    <div class="event-container">
      <p class="page-title">Events</p>
      <div class="event-lists">
        <event-card v-for="(e, i) in 10" :key="i" />
      </div>
    </div>
  </div>
</template>

<script>
import EventCard from '~/components/EventCard.vue'
export default {
  name: 'EventPage',
  components: { EventCard },
}
</script>

<style lang="scss" scoped>
.event-container {
  background: #000;
  height: 100%;
  width: 100vw;
  padding: 4rem 3rem 2rem 3rem;
  color: #fff;

  .page-title {
    font-family: 'Poppins', sans-serif;
    font-weight: bold;
    font-size: 3rem;
    letter-spacing: 0.02em;
    width: fit-content;
  }

  .event-lists {
    margin-top: 5rem;
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
  }
}

@media all and (max-width: '912px') {
  .event-container {
    padding: 4rem 2rem 2rem 2rem;

    .page-title {
      font-size: 2.5rem;
    }
  }
}
</style>
