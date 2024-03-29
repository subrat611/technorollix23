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
        <p>Glorify yourself through your talent.</p>
      </div>

      <!-- event rules and regulation -->
      <div class="detail-rules">
        <h2>{{ 'Rules of the event'.toUpperCase() }}</h2>
        <ul>
          <li>It is an individual event i.e. one entry per registration.</li>
          <li>
            Registrations are allowed in one category per individual only.
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
          <li>No entries without registration.</li>
          <li>Decision of the jury will be final.</li>
        </ul>
      </div>

      <!-- rounds of event -->
      <div class="detail-judg">
        <h2>{{ 'Rounds of the event'.toUpperCase() }}</h2>
        <p>
          The number of rounds will be decided based on the entries. This will
          be intimated later. However, in final round 15- 20 individuals will be
          given a chance to showcase their talent.
        </p>
        <ul>
          <li>Form</li>
          <li>Interview</li>
          <li>Task 1: - Fitness Round - One round of college campus</li>
          <li>Task 2: - Slippery surface and to bring tomato</li>
          <li>Task 3: - Tug of war</li>
          <li>Task 4: - Arm wrestling</li>
          <li>Semi final</li>
          <li>Final</li>
        </ul>
      </div>

      <!-- Judgemental Criteria -->
      <div class="detail-judg">
        <h2>{{ 'Judgemental Criteria'.toUpperCase() }}</h2>
        <ul>
          <li>Clarity in performance</li>
          <li>Hard work</li>
          <li>Confidence</li>
          <li>Discipline</li>
          <li>Fitness</li>
          <li>Time duration for an event</li>
        </ul>
        <p>
          Note <br />
          1. Initial round will be judged by in-house faculty. <br />
          2. Final round will be judged by External judges as well as in-house
          faculty. <br />
          3. The parameter of judgment may change which will be intimated later.
        </p>
      </div>

      <!-- prizes -->
      <div class="detail-judg">
        <h2>{{ 'prizes'.toUpperCase() }}</h2>
        <ul class="prize-wrapper">
          <li class="prize">
            <nuxt-img
              src="/prize1.png"
              format="webp"
              width="130"
              height="130"
            />
            <span>1<sup>st</sup> Prize</span>
          </li>
          <li class="prize">
            <nuxt-img
              src="/prize2.png"
              format="webp"
              width="130"
              height="130"
            />
            <span>2<sup>nd</sup> Prize</span>
          </li>
          <li class="prize">
            <nuxt-img
              src="/prize3.png"
              format="webp"
              width="130"
              height="130"
            />
            <span>3<sup>rd</sup> Prize</span>
          </li>
          <li class="prize">
            <nuxt-img
              src="/certificate.png"
              format="webp"
              width="90"
              height="90"
            />
            <span style="text-align: center">
              Certificate of appreciation<br />for all the participants
            </span>
          </li>
        </ul>
      </div>

      <!-- venue -->

      <div class="detail-judg">
        <h2>{{ 'venue'.toUpperCase() }}</h2>
        <p>
          <b>Near volleyball court (or any other to be notified later)</b>
        </p>
      </div>

      <!-- contact details -->
      <div class="detail-contact">
        <h2>{{ 'Contact details'.toUpperCase() }}</h2>
        <event-details :teams="event.teams" />
      </div>

      <div class="reg-btn">
        <a href="https://sites.google.com/view/opju-reg/home" target="_blank">
          <button>register</button>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'RoadiesEventPage',
  data() {
    return {
      event: {
        name: 'ROADIES',
        img: 'roadies.png',
        event_desc:
          'OPJU brings you the platform of ROADIES to showcase your talents and let the world celebrate your identity.',
        teams: [
          { img: 'pratik.jpg', name: 'Pratik Singh', call: '7004517121' },
          { img: 'deveshpatel.jpg', name: 'Devesh Patel', call: '9669600098' },
          { img: 'sv.jpg', name: 'S V Saishankar ', call: '7049268306' },
          { img: 'ankitraj.jpg', name: 'Ankit Raj', call: '7004610158' },
          { img: 'rishikasahu.jpg', name: 'Rishika Sahu', call: '8224099894' },
        ],
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

      .prize-wrapper {
        display: flex;
        justify-content: space-evenly;
        flex-wrap: wrap;
        .prize {
          width: fit-content;
          display: flex;
          flex-direction: column;
          justify-content: center;
          align-items: center;

          span {
            font-size: 1.2rem;
            font-weight: bold;
            letter-spacing: 0.03em;
          }
        }
      }
    }

    .detail-contact {
      margin-top: 1.5rem;
    }

    .reg-btn {
      margin: 3rem 0;

      button {
        margin-top: 1rem;
        width: fit-content;
        padding: 1rem 1.5rem;
        font-size: 1.2rem;
        font-weight: bolder;
        border: none;
        color: #fff;
        text-transform: capitalize;
        border-radius: 3px;
        outline: none;
        letter-spacing: 0.05em;
        font-family: 'Montserrat', sans-serif;
        font-weight: 700;
        cursor: pointer;

        background: rgba(63, 194, 255, 0.11);
        border-radius: 7px;
        box-shadow: 0 4px 30px rgba(104, 104, 104, 0.1);
        backdrop-filter: blur(3.3px);
        -webkit-backdrop-filter: blur(3.3px);
        border: 1px solid rgba(255, 217, 252, 0.2);
        -webkit-backdrop-filter: blur(3.3px);

        transition: all 200ms ease-out;

        &:hover {
          background: rgba(63, 194, 255, 0.212);
          border-radius: 7px;
          box-shadow: 0 4px 30px rgba(104, 104, 104, 0.1);
          backdrop-filter: blur(3.3px);
          -webkit-backdrop-filter: blur(3.3px);
          border: 1px solid rgba(255, 217, 252, 0.2);
          -webkit-backdrop-filter: blur(3.3px);
        }
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
