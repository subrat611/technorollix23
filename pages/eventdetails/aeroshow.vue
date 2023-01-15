<template>
  <div class="event-details-wrapper">
    <back-btn />
    <div class="detail-container">
      <!-- img -->
      <div class="detail-img">
        <nuxt-img :src="'/event/' + event.img" />
        <div class="overlay"></div>
      </div>

      <!-- header -->
      <div class="detail-header">
        <div class="header-one">
          <h1>{{ event.name.toUpperCase() }}</h1>
        </div>
      </div>

      <!-- event desc -->
      <div class="detail-info">
        <p>{{ event.event_desc }}</p>
      </div>

      <!-- event theme -->
      <div class="detail-rules">
        <h2>{{ 'theme'.toUpperCase() }}</h2>
        <p>
          Innovation, transformation and vitalizing equipment's, knowledgeSkill
        </p>
      </div>

      <!-- event rules and regulation -->
      <div class="detail-rules">
        <h2>{{ 'Rules and Regulation'.toUpperCase() }}</h2>
        <ul>
          <li>
            2 chances will be given in case of failures of batteries or other
            part
          </li>
          <li>3-4 A-cell battery's max (2200-3000 mAh).</li>
          <li>Drone weight should be less than or equal to 2 kilograms.</li>
          <li>Drone size should be 14 inches or less.</li>
          <li>Number of propellers should be in between 4 to 8.</li>
          <li>No factory made drone should be allowed.</li>
          <li>
            All Participants should be there at the venue 30mins before the
            event starts.
          </li>
        </ul>
      </div>

      <!-- event rules and regulation -->
      <div class="detail-rules">
        <h2>{{ 'rounds of event'.toUpperCase() }}</h2>
        <ul>
          <li>
            1<sup>st</sup> Round: Accuracy test
            <p>
              Testing the skills of drone in moving forward, backward, as well
              as elevation and demotion.
            </p>
          </li>
          <li>
            2<sup>nd</sup> Round: Obstacle avoiding test
            <p>
              Testing the skills of drone to avoid the obstacles and reach its
              destinationas quick as possible.
            </p>
          </li>
          <li>
            3<sup>3rd</sup> Round: Final Round
            <p>Testing all the abilities of the Drone to max.</p>
          </li>
          <li>
            <b>Win the round by unlocking all your potential and skill</b>
          </li>
        </ul>
      </div>

      <!-- event prizes -->
      <div class="detail-rules">
        <h2>{{ 'prizes'.toUpperCase() }}</h2>
        <ul>
          <li>1 st - Rs. 5000</li>
          <li>2 nd - Rs. 3000</li>
          <li>3 rd - Rs. 2000</li>
          <li>
            Consolation Prize – Rs. 1000 (only for a single participant/group)
          </li>
        </ul>
      </div>

      <!-- Judgemental Criteria -->
      <div class="detail-judg">
        <h2>{{ 'Judgemental Criteria'.toUpperCase() }}</h2>
        <p>
          <b
            >All rounds are Elimination rounds. Final round will be decided by
            thedronethat wins the race first by time.</b
          >
        </p>
      </div>

      <!-- venue -->

      <div class="detail-judg">
        <h2>{{ 'venue'.toUpperCase() }}</h2>
        <p>
          <b>Basketball ground</b>
        </p>
      </div>

      <!-- contact details -->
      <div class="detail-contact">
        <h2>{{ 'Contact details'.toUpperCase() }}</h2>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'YuvaSadanEventPage',
  data() {
    return {
      event: {
        name: 'Aero Show',
        img: '',
        event_desc:
          'It is a drone racing event captivating the knowledge of Mechanical, Electrical and Cs skills based on your drone. Your drone wouldbetestedrigorously across the event through various rounds. Showyour skillsandabilities to bring out max potential of your UAVs.',
      },
    }
  },
}
</script>

<style lang="scss" scoped>
li {
  list-style: square;
}
.event-details-wrapper {
  background: #000;
  color: #fff;
  min-height: 100vh;
  max-height: 100%;
  background-image: linear-gradient(to bottom, #00388b4f, #6b08663b);

  .detail-container {
    max-width: 1480px;
    margin: 0 auto;

    padding: 5rem 1.1rem;
    display: flex;
    flex-direction: column;

    .detail-img {
      width: 100%;
      height: 420px;
      position: relative;
      box-shadow: rgba(17, 12, 46, 0.15) 0px 48px 100px 0px;

      img {
        width: 100%;
        height: 100%;
        border-radius: 4px;
        box-shadow: rgba(0, 0, 0, 0.1) 0px 4px 12px;
      }

      // overlay edit here
    }

    .detail-header {
      margin-top: 1rem;

      .header-one {
        margin: 1rem 0;

        h1 {
          font-family: 'Poppins', sans-serif;
          background: -webkit-linear-gradient(#ff0084, #e3e3e3);
          background-clip: text;
          -webkit-background-clip: text;
          -webkit-text-fill-color: transparent;
          padding: 0.3rem 0;
        }
      }
    }

    .detail-info {
      background: rgba(63, 194, 255, 0.11);
      border-radius: 7px;
      box-shadow: 0 4px 30px rgba(104, 104, 104, 0.1);
      backdrop-filter: blur(3.3px);
      -webkit-backdrop-filter: blur(3.3px);
      border: 1px solid rgba(255, 217, 252, 0.2);
      padding: 1rem;

      p {
        font-family: 'Roboto', sans-serif;
        font-size: 1.1rem;
        line-height: 1.6rem;
      }
    }

    .detail-rules,
    .detail-judg {
      margin-top: 1.5rem;

      h2 {
        padding: 1rem 0;
        font-family: 'Roboto', sans-serif;
      }

      p {
        line-height: 1.4rem;
        padding: 1rem 1rem;
        background: rgba(63, 194, 255, 0.11);
        border-radius: 7px;
        box-shadow: 0 4px 30px rgba(104, 104, 104, 0.1);
        backdrop-filter: blur(3.3px);
        -webkit-backdrop-filter: blur(3.3px);
        border: 1px solid rgba(255, 217, 252, 0.2);
      }

      ul > li {
        padding: 0.3rem 0;
        margin-left: 1rem;
        font-size: 1.1rem;
        font-family: 'Roboto', sans-serif;
        line-height: 1.6rem;
      }
    }

    .detail-contact {
      margin-top: 1.5rem;
    }
  }
}

@media all and (max-width: '912px') {
  .event-details-wrapper {
    .detail-container {
      padding: 7rem auto 5rem auto;

      .detail-img {
        height: 20vh;
      }
    }
  }
}
</style>
