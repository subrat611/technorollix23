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
        <p>Unleash your Entrepreneurial Caliber</p>
      </div>

      <!-- event rules and regulation -->
      <div class="detail-rules">
        <h2>{{ 'Rules and Rounds'.toUpperCase() }}</h2>
        <ul>
          <li>
            The competition is open for teams comprising graduate & postgraduate
            students.
          </li>
          <li>
            A maximum of four members (Founders) are permitted in a team. No
            change of team structure is permitted after the team is registered.
          </li>
          <li>One participant cannot be part of more than one team.</li>
          <li>
            One of the team members should be registered as the team leader.
          </li>
          <li>
            There will be a Shortlisting of Participants, at the time of
            registration participants are required to mention about their
            start-up plan, Only selected start-up plan/start-ups will be
            considered for Final Presentation in front of the Panel Members.
          </li>
          <li>
            Maximum 15 slides of power point presentation are allowed for
            presentaing the Start-up Plan/Start-up (If Any).
          </li>
          <li>
            Maximum 15 minutes per team will be giben for presenting the
            start-up plan/start-up.
          </li>
          <li>Participants must carry their Laptop for presentation.</li>
          <li>
            Selected Start-ups may be considered for Incubation under OPJU
            Innovation Center.
          </li>
        </ul>
      </div>

      <!-- Judgemental Criteria -->
      <div class="detail-judg">
        <h2>{{ 'Judgemental Criteria'.toUpperCase() }}</h2>
        <p>
          <b
            >Parameters will be set by the Organizing Committee after the
            experts/start-up founders.</b
          >
        </p>
      </div>

      <!-- prizes -->
      <div class="detail-judg">
        <h2>{{ 'prizes'.toUpperCase() }}</h2>
        <p>
          1. First Prize - Rs. 15,000 <br />
          2. Second Prize - Rs. 10,000 <br />
          3. Third Prize - Rs. 5000 <br />
        </p>
      </div>

      <!-- venue -->

      <div class="detail-judg">
        <h2>{{ 'venue'.toUpperCase() }}</h2>
        <p>
          <b>Live Classroom</b>
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
  name: 'SharkTankEventPage',
  data() {
    return {
      event: {
        name: 'Shark Tank (Start-up Competititon)',
        img: '',
        event_desc:
          'The purpose of the event is to provide students with practical experience so they may present their Start-up plans in one of two categories—seed or early-stage. Based on the market opportunity and concept validity of the plan, judges will assess the seed category. Entrepreneurs in the early-stage category, who have more developed company models, will be judged. The best pitches will walk away with Cash Prizes and Mentoring Opportunities.',
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
