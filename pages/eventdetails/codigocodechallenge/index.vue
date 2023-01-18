<template>
  <div class="event-details-wrapper">
    <back-btn />
    <div class="main-wrapper">
      <div class="card-wrapper">
        <div
          v-for="({ param, eventName, eventDesc }, i) in events"
          :key="i"
          class="card-container"
        >
          <div class="card-img"><nuxt-img src="/event/codigo.png" /></div>
          <div class="card-content">
            <p class="card-title">{{ eventName.toUpperCase() }}</p>
            <p class="card-desc">
              {{ eventDesc }}
              <nuxt-link :to="`/eventdetails/codigocodechallenge/` + param"
                >...more</nuxt-link
              >
            </p>
            <nuxt-link :to="`/eventdetails/codigocodechallenge/` + param">
              <button>register</button>
            </nuxt-link>
          </div>
        </div>
      </div>
      <div class="details-wrapper">
        <h2>RULES AND REGULATIONS OF CODIGO</h2>
        <ul>
          <li>
            1. No participant is allowed to carry mobile or any electronic
            gadgets during the competition.
          </li>
          <li>2. Sitting arrangement will be decided by event organizers.</li>
          <li>
            3. If due to any circumstances, one could not be present during the
            event then the participant will be eliminated.
          </li>
          <li>
            4. If any participant is found using Unfair means, necessary action
            as per the rules of the event shall be taken.
          </li>
          <li>5. Both events will be held on the same day simultaneously.</li>
          <li>6. No participants can take part in both the sub-events.</li>
          <li>7. After Every round point will be announced.</li>
          <li>
            8. Rules and Regulations may change without prior notice, by the
            Event organizers.
          </li>
          <li>9. No extra time will be given in any of the events.</li>
          <li>
            10. The event will be held on any Online platform and disclosed
            right before the event.
          </li>
        </ul>
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
          param: 'crackit',
          eventName: 'Crack it if you can (coding base)',
          eventDesc:
            'The Codigo, Technorollix 23, OPJU is an event to check your problem-solving skill, analysis skills, and thinking logically.',
        },
        {
          param: 'thinkin',
          eventName: 'Think in UI/UX (designing)',
          eventDesc:
            'The Codigo, Technorollix 23, OPJU is an event to test the strategy of comprehensive experience in Visual Designing of students.',
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
  justify-content: center;

  .main-wrapper {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 80%;

    .card-wrapper {
      width: 100%;
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
            text-transform: capitalize;
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

    .details-wrapper {
      width: 95%;
      padding: 1rem;
      margin-top: 1rem;

      h2 {
        text-align: center;
        padding: 1rem 0;
        font-family: 'Roboto', sans-serif;
      }

      ul > li {
        padding: 0.3rem 0;
        margin-left: 1rem;
        font-size: 1.1rem;
        font-family: 'Roboto', sans-serif;
        line-height: 1.6rem;
      }
    }
  }
}

@media all and (max-width: '1156px') {
  .event-details-wrapper {
    .main-wrapper {
      width: 100%;
      .card-wrapper {
        width: 100%;
        margin: 5rem 0 0 0;
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
}
</style>
