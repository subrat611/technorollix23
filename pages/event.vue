<template>
  <div>
    <nav-bar />
    <nav-bar-two />
    <div class="event-container">
      <p class="page-title">Events</p>
      <div class="event-lists">
        <event-card
          v-for="(event, i) in events"
          :key="i"
          :event-name="event.event_name"
          :event-desc="event.event_desc"
          :event-img="event.event_img"
          :index="i"
        />
      </div>
    </div>
  </div>
</template>

<script>
import EventCard from '~/components/EventCard.vue'
import NavBarTwo from '~/components/NavBarTwo.vue'
export default {
  name: 'EventPage',
  components: { EventCard, NavBarTwo },
  data() {
    return {
      events: [
        {
          event_name: 'shark tank',
          event_desc:
            'The purpose of the event is to provide students with practical experience so they may present their Start-up plans in one of two categories—seed or early-stage. Based on the market',
          event_img: '',
        },
        {
          event_name: 'KalaKriti',
        },
        {
          event_name: 'antaragni',
          event_img: '',
        },
        {
          event_name: 'ideathon',
          event_desc:
            'An Ideathon is a short, engaging brainstorming event where individuals from different backgrounds address some of the most pressing challenges of our time. Individuals',
          event_img: '',
        },
        {
          event_name: 'Yuva Sadan',
          event_desc:
            'The yuva sadan, technorollix, OPJU is an event to test the leadership and debating qualities of participants, stretching across different world wide issues related topics.',
          event_img: 'yuva.jpg',
        },
        {
          event_name: 'robovation',
          event_desc:
            'Design a robot wire or wireless within the specified dimensions that can operated manually and can travel through all turns of the track. The robot that will complete',
          event_img: 'robovation.jpg',
        },
        {
          event_name: 'lan gaming',
          event_img: '',
        },
        {
          event_name: 'battle of bands',
          event_desc:
            "Battle of Bands is a competition between musical bands to show their talent and compete against each other. It's designed to bring college students together and inspire",
          event_img: '',
        },
        {
          event_name: 'brainy escape',
          event_desc:
            'A fun and exciting game for you to show your knowledge and intellectual skills and win exciting prizes. With different rounds to test your different skills and problem solving aptitude',
          event_img: 'quiz.jpg',
        },
        {
          event_name: 'tech lab',
          event_desc:
            'Tech lab is one of the most prestigious event of Technorollix,which is the biggest tech festival of central India.The event shows the creativity and potential of bright minds from ',
          event_img: 'techlab.jpg',
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
          event_desc:
            'The Codigo, Technorollix 23, OPJU is an event to check your problem-solving skill, analysis skills, and thinking logically. To test the strategy of comprehensive experience ',
          event_img: 'codigo.png',
        },
        {
          event_name: 'talent hunt',
          event_desc:
            'OPJU brings you the platform of TALENT HUNT to showcase your talents and let the world celebrate your identity. You can apply in any of the following categories: Magic, Story telling',
          event_img: '',
        },
        {
          event_name: 'aero show',
          event_desc:
            'It is a drone racing event captivating the knowledge of Mechanical, Electrical and Cs skills based on your drone. Your drone wouldbetestedrigorously across the event through',
        },
      ],
    }
  },
}
</script>

<style lang="scss" scoped>
.event-container {
  background: #000;
  background-image: linear-gradient(to bottom, #41195f2d, #000000);
  height: 100%;
  width: 100vw;
  padding: 8rem 3rem 2rem 3rem;
  color: #fff;

  .page-title {
    font-family: 'Poppins', sans-serif;
    font-weight: bold;
    font-size: 3rem;
    letter-spacing: 0.02em;
    width: fit-content;
    background: -webkit-linear-gradient(#b6b6b6, #e3e3e3e5);
    background-clip: text;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
  }

  .event-lists {
    margin-top: 5rem;
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
  }
}

@media all and (max-width: '1248px') {
  .event-container {
    padding: 4rem 2rem 2rem 2rem;
  }
}

@media all and (max-width: '912px') {
  .event-container {
    .page-title {
      font-size: 2.5rem;
    }

    .event-lists {
      margin-top: 3rem;
    }
  }
}
</style>
