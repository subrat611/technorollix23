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

      <!-- event categories -->
      <div class="detail-rules">
        <h2>You can apply in any of the following games</h2>
        <div class="flex justify-content-start">
          <ul>
            <li>Valorant</li>
            <li>Clash Royal</li>
            <li>Call of Duty</li>
            <li>Taken</li>
            <li>Free Fire MAX</li>
          </ul>
        </div>
      </div>

      <!-- event theme -->
      <div class="detail-rules">
        <h2>{{ 'theme'.toUpperCase() }}</h2>
        <p>
          A recipe has no soul you as the cook must bring soul to the recipe.
        </p>
      </div>

      <!-- event rules and regulation -->
      <div class="detail-rules">
        <h2>{{ 'Rules of the event'.toUpperCase() }}</h2>
        <ul>
          <li>
            It is a group event i.e. group wise registration only 2 members.
          </li>
          <li>
            Registrations are allowed from other institute (outsider of OPJU)
            registration fee per group 100 rs.
          </li>
          <li>
            UG and PG students (Age 18- below 30) allowed of colleges /
            university.
          </li>
          <li>
            Performance should be within the time limit which will be intimated
            later.
          </li>
          <li>
            Contents should not be offensive, politically driven, gender biased,
            personal comments or any sensitive topic.
          </li>
          <li>No abusive language.</li>
          <li>Costumes should be appropriate.</li>
          <li>No entries without registration.</li>
          <li>Decision of the jury will be final.</li>
          <li>Participants should be cooperative to the team member.</li>
          <li>Result will be announced on the same date.</li>
        </ul>
      </div>

      <!-- rounds of event -->
      <div class="detail-judg">
        <h2>{{ 'Rounds of the event'.toUpperCase() }}</h2>
        <p>
          The number of rounds will be decided based on the entries. This will
          be intimated later.
        </p>
      </div>

      <!-- Judgemental Criteria -->
      <div class="detail-judg">
        <h2>{{ 'Judgemental Criteria'.toUpperCase() }}</h2>
        <ul>
          <li>Taste Preference</li>
          <li>Plating</li>
          <li>Confidence</li>
          <li>Performance</li>
        </ul>
        <p>
          Note <br />
          1. Each parameter contains 10 marks.<br />
          2. The parameter of judgment may change which will be intimated later.
          <br />
        </p>
      </div>

      <!-- prizes -->
      <div class="detail-judg">
        <h2>{{ 'prizes'.toUpperCase() }}</h2>
        <p>
          1. First, Second and Third<br />
          2. Three consolation prizes <br />
          3. Certificate of appreciation for all the participants.
        </p>
      </div>

      <!-- venue -->

      <div class="detail-judg">
        <h2>{{ 'venue'.toUpperCase() }}</h2>
        <p>
          <b>Cafeteria ground floor</b>
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
  name: 'LanGamingEventPage',
  data() {
    return {
      event: {
        name: 'FOOD FIESTA',
        img: '',
        event_desc:
          'OPJU brings you an extraordinary platform “FOOD FIESTA” to showcase your talents and let the world know your taste.',
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
        margin: 0.5rem 0;
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
