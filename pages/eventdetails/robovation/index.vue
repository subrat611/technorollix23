<template>
  <div class="event-details-wrapper">
    <back-btn />
    <div class="card-wrapper">
      <div
        v-for="({ eventName, eventDesc }, i) in events"
        :key="i"
        class="card-container"
      >
        <div class="card-img"><nuxt-img src="/event/robovation.jpg" /></div>
        <div class="card-content">
          <p class="card-title">{{ eventName.toUpperCase() }}</p>
          <p class="card-desc">
            {{ eventDesc }}
            <nuxt-link
              :to="`/eventdetails/robovation/` + eventName.replace(/\s/g, '')"
              >...more</nuxt-link
            >
          </p>
          <nuxt-link :to="`/eventdetails/` + eventName">
            <button>register</button>
          </nuxt-link>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'EventCard',
  data() {
    return {
      events: [
        {
          eventName: 'Robo Race',
          eventDesc:
            'Design a wired/wireless manually controlled robot which should be able to travel on all the',
        },
        {
          eventName: 'Robo Soccer',
          eventDesc:
            'Robo soccer is one of famous challenges of robovation in this event teams comes with single',
        },
      ],
    }
  },
}
</script>

<style lang="scss" scoped>
a {
  color: #e5e5e5;
}

.event-details-wrapper {
  background: #000;
  color: #fff;
  min-height: 100vh;
  max-height: 100%;
  background-image: linear-gradient(to bottom, #00388b4f, #6b08663b);
  display: flex;
  flex-direction: column;
  justify-content: center;

  .card-wrapper {
    width: 70%;
    margin: 0 auto;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;

    .card-container {
      width: 400px;
      background: rgba(63, 194, 255, 0.11);
      border-radius: 7px;
      box-shadow: 0 4px 30px rgba(104, 104, 104, 0.1);
      backdrop-filter: blur(3.3px);
      -webkit-backdrop-filter: blur(3.3px);
      border: 1px solid rgba(255, 217, 252, 0.2);
      padding: 1.5rem 1rem;
      display: flex;
      flex-direction: column;
      justify-content: center;

      .card-img {
        width: 100%;

        img {
          border-radius: 6px;
          width: 100%;
        }
      }
      .card-content {
        width: 100%;

        .card-title {
          font-family: 'Montserrat', sans-serif;
          font-size: 1.4rem;
          padding: 0.7rem 0;
          font-weight: 600;
          text-transform: capitalize;
        }

        .card-desc {
          line-height: 1.4rem;
          padding: 0 0.5rem 0 0;
          color: #e5e5e5;
          font-family: 'Montserrat', sans-serif;

          a {
            text-decoration: none;
            font-weight: bold;
            color: #00b4d8;
          }
        }

        button {
          margin-top: 1rem;
          width: 100%;
          padding: 0.7rem;
          font-size: 1.2rem;
          border: none;
          color: #fff;
          text-transform: capitalize;
          border-radius: 3px;
          outline: none;
          letter-spacing: 0.02em;
          font-family: 'Montserrat', sans-serif;
          font-weight: 500;
          cursor: pointer;

          background: rgba(255, 255, 255, 0.116);
          box-shadow: 0 4px 30px rgba(255, 255, 255, 0.1);
          backdrop-filter: blur(3.3px);
          -webkit-backdrop-filter: blur(3.3px);

          transition: all 200ms ease-out;

          &:hover {
            background: rgba(255, 255, 255, 0.253);
            box-shadow: 0 4px 30px rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(3.3px);
            -webkit-backdrop-filter: blur(3.3px);
          }
        }
      }
    }
  }
}

@media all and (max-width: '1156px') {
  .event-details-wrapper {
    .card-wrapper {
      width: 100%;
      margin: 5rem 0;
      padding: 0 1rem;

      .card-container {
        width: 100%;
        margin: 1rem 0.2rem;
        padding: 1rem;

        .card-content {
          .card-title {
            font-size: 1.2rem;
          }

          .card-desc {
            font-size: 0.9rem;
            line-height: 1.3rem;
          }

          button {
            font-size: 1rem;
          }
        }
      }
    }
  }
}
</style>
