<template>
  <div>
    <nav-bar />
    <div class="event-container">
      <p class="page-title">Events</p>
      <div class="event-lists">
        <event-card
          v-for="(event, i) in events"
          :key="i"
          :event-name="event.event_name"
        />
      </div>
    </div>
  </div>
</template>

<script>
import EventCard from '~/components/EventCard.vue'
export default {
  name: 'EventPage',
  components: { EventCard },
  data() {
    return {
      events: [
        {
          event_name: 'shart tank',
          event_desc: '',
        },
        {
          event_name: 'KalaKriti',
          event_desc: '',
        },
        {
          event_name: 'antaragni',
          event_desc: '',
        },
        {
          event_name: 'ideathon',
          event_desc: '',
        },
        {
          event_name: 'YuvaSadan',
          event_desc: '',
        },
        {
          event_name: 'robovation',
          event_desc: '',
        },
        {
          event_name: 'lan gaming',
          event_desc: '',
        },
        {
          event_name: 'battle of bands',
          event_desc: '',
        },
        {
          event_name: 'brainy escape',
          event_desc: '',
        },
        {
          event_name: 'tech lab',
          event_desc: '',
        },
        {
          event_name: 'roadies',
          event_desc: '',
        },
        {
          event_name: 'aaghaaz the fashion show',
          event_desc: '',
        },
        {
          event_name: 'food fiesta',
          event_desc: '',
        },
        {
          event_name: 'codigo code challenge',
          event_desc: '',
        },
        {
          event_name: 'talent hunt',
          event_desc: '',
        },
        {
          event_name: 'aero-show',
          event_desc: '',
        },
      ],
    }
  },
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
