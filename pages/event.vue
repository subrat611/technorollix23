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
          :event-desc="event.event_desc"
          :event-img="event.event_img"
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
        },
        {
          event_name: 'KalaKriti',
        },
        {
          event_name: 'antaragni',
        },
        {
          event_name: 'ideathon',
        },
        {
          event_name: 'YuvaSadan',
          event_desc:
            'The yuva sadan, technorollix, OPJU is an event to test the leadership and debating qualities of participants, stretching across different world wide issues related topics.',
          event_img: 'yuva.jpg',
        },
        {
          event_name: 'robovation',
        },
        {
          event_name: 'lan gaming',
        },
        {
          event_name: 'battle of bands',
        },
        {
          event_name: 'brainy escape',
          event_desc:
            'A fun and exciting game for you to show your knowledge and intellectual skills and win exciting prizes. With different rounds to test your different skills and problem solving aptitude',
        },
        {
          event_name: 'tech lab',
        },
        {
          event_name: 'roadies',
        },
        {
          event_name: 'aaghaaz the fashion show',
        },
        {
          event_name: 'food fiesta',
        },
        {
          event_name: 'codigo code challenge',
        },
        {
          event_name: 'talent hunt',
        },
        {
          event_name: 'aero-show',
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

    .event-lists {
      margin-top: 3rem;
    }
  }
}
</style>
