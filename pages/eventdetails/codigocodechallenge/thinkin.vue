<template>
  <div class="event-details-wrapper">
    <back-btn />
    <div class="detail-container">
      <!-- img -->
      <div class="detail-img">
        <nuxt-img src="/event/thinkin.png" />
        <div class="overlay"></div>
      </div>

      <!-- header -->
      <div class="detail-header">
        <div class="header-one">
          <h1>{{ event.name.toUpperCase() }}</h1>
        </div>
      </div>

      <!-- overview -->
      <div class="detail-info">
        <h2>{{ 'About Think UI (designing)'.toUpperCase() }}</h2>
        <br />
        <p>Each round consist of 100 points.</p>
      </div>

      <!-- Round 1 (Qualification round) -->
      <div class="detail-round">
        <h2>Round 1 (Qualification Round)</h2>
        <ul>
          <li>
            In this round, we will provide you with choices of components you
            want to design and you will be given 30 minutes to design that
            particular component.
          </li>
        </ul>
      </div>

      <!-- Round 2(Elimination Round) -->
      <div class="detail-round">
        <h2>Round 2(Elimination Round)</h2>
        <ul>
          <li>
            In this round, you will have to design a landing page for a website.
            There will be choices in this round also.
          </li>
        </ul>
      </div>

      <!-- Round 3 (Final Round) -->
      <div class="detail-round">
        <h2>Round 3 (Final Round)</h2>
        <ul>
          <li>
            For this round, you will have 3 hours of time in which you will have
            to design a complete website.
          </li>
          <li>
            There will be no choices in this round the niche of the website will
            be disclosed 30 minutes before the round starts.
          </li>
        </ul>
      </div>

      <!-- RULES AND REGULATIONS: -->
      <div class="detail-rules">
        <h2>RULES AND REGULATIONS</h2>
        <ul>
          <li>Participants have to bring their own laptops.</li>
          <li>
            You can use any website for inspiration to design your website.
          </li>
          <li>You will have to design on Figma (UI design platform).</li>
          <li>
            You are not allowed to copy any design if found you will be
            disqualified.
          </li>
          <li>
            Unethical behavior could lead to disqualification. Faculty
            coordinators have all the rights to take final decisions for any
            matter during the event. and Judge's decision will be considered
            final.
          </li>
          <li>
            Certificates of Participation will be given to all the teams
            participating in the event but not to the teams that get
            disqualified due to disobeying any of the competition rules.
          </li>
        </ul>
      </div>

      <div class="detail-info">
        <div class="header-one">
          <p>
            Coordination committee reserves the right to add or update any rule.
          </p>
        </div>
      </div>

      <!-- contact -->
      <div class="detail-contact">
        <h2>EVENT MANAGER</h2>
      </div>

      <!-- robo soccer -->
    </div>
  </div>
</template>

<script>
export default {
  name: 'ThinkInEventPage',
  data() {
    return {
      event: {
        name: 'Think UI (designing)',
        img: 'codigo.png',
        event_desc:
          'The Codigo, Technorollix 23, OPJU is an event to test the strategy of comprehensive experience in Visual Designing of students.',
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

      h2 {
        padding: 1rem 0;
      }

      .header-one {
        margin: 1rem 0;

        h1 {
          font-family: 'Poppins', sans-serif;
          background: -webkit-linear-gradient(#ff0084, #e3e3e3);
          background-clip: text;
          -webkit-background-clip: text;
          -webkit-text-fill-color: transparent;
        }

        h1,
        p {
          padding: 0.3rem 0;
        }

        p {
          font-size: 1.1rem;
          font-family: 'Roboto', sans-serif;
          line-height: 1.5rem;
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

    .detail-spec,
    .detail-power,
    .detail-rules,
    .detail-game-rules,
    .detail-round,
    .detail-round,
    .detail-round {
      margin-top: 1.5rem;

      h2 {
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

    .detail-track {
      margin-top: 1.5rem;

      p {
        margin-top: 1rem;
        padding: 0.2rem 0;
        font-size: 1.1rem;
        font-family: 'Roboto', sans-serif;
        line-height: 1.6rem;
      }
    }

    .detail-contact {
      margin-top: 1.5rem;
    }

    // robo soccer
    .detail-overview {
      background: rgba(63, 194, 255, 0.11);
      border-radius: 7px;
      box-shadow: 0 4px 30px rgba(104, 104, 104, 0.1);
      backdrop-filter: blur(3.3px);
      -webkit-backdrop-filter: blur(3.3px);
      border: 1px solid rgba(255, 217, 252, 0.2);
      padding: 1rem;

      h2 {
        padding: 0.2rem 0;
      }

      p {
        font-family: 'Roboto', sans-serif;
        font-size: 1.1rem;
        line-height: 1.6rem;
      }
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
