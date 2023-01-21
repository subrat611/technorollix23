<template>
  <div class="event-details-wrapper">
    <back-btn />
    <div class="detail-container">
      <!-- img -->
      <div class="detail-img">
        <nuxt-img src="/event/crackit.png" />
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
        <h2>{{ 'About Crack It If You Can'.toUpperCase() }}</h2>
        <br />
        <p>The total point throughout the event is 300(60+60+80+100).</p>
      </div>

      <!-- Round 1 (Rapid or Qualifying round) -->
      <div class="detail-round">
        <h2>Round 1 (Rapid or Qualifying round)</h2>
        <ul>
          <li>
            There will be 15 Questions from which you have to answer 10
            questions to qualify this round in 15 minutes.
          </li>
        </ul>
      </div>

      <!-- Round 2 (Bug Finding or logic Based) -->
      <div class="detail-round">
        <h2>Round 2 (Bug Finding or logic Based)</h2>
        <ul>
          <li>
            There will be 10 questions on 20 minutes of a time trial. The
            participants have to perform in pairs.
          </li>
        </ul>
      </div>

      <!-- Round 3 (One Vs One Round): -->
      <div class="detail-round">
        <h2>Round 3 (One Vs One Round)</h2>
        <ul>
          <li>
            The participants will be divided into pairs and they will be
            competing with each other.
          </li>
          <li>
            There will be 5 questions out of which you have to answer any 4
            questions within 45 min of a time trial.
          </li>
        </ul>
      </div>

      <!-- Round 4 (Final round) -->
      <div class="detail-round">
        <h2>Round 4 (Final round)</h2>
        <ul>
          <li>There will be 3 questions in 90 minutes of a time trial.</li>
        </ul>
      </div>

      <!-- RULES AND REGULATIONS: -->
      <div class="detail-rules">
        <h2>RULES AND REGULATIONS</h2>
        <ul>
          <li>Participants have to bring their own laptops.</li>
          <li>
            Regarding the coding platform you will get to know it right before
            the competition.
          </li>
          <li>
            No participant is allowed to leave the competition in the middle.
          </li>
          <li>Round 1 and 4 is played individually.</li>
          <li>
            Rounds 2 and 3 will be played in pairs and pairs will be decided by
            the event organizers.
          </li>
          <li>
            You can use any of the language from these four java , python ,c++
            and c.
          </li>
        </ul>
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
  name: 'CrackItEventPage',
  data() {
    return {
      event: {
        name: 'Crack it if you can (coding base)',
        img: 'codigo.png',
        event_desc:
          'The Codigo, Technorollix 23, OPJU is an event to check your problem-solving skill, analysis skills, and thinking logically.',
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
