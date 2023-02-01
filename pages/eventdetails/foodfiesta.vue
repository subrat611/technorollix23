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
          A recipe has no soul you as the cook, must bring soul to the recipe.
        </p>
      </div>

      <!-- event rules and regulation -->
      <div class="detail-rules">
        <h2>{{ 'Rules of the event'.toUpperCase() }}</h2>
        <ul>
          <li>Teams will be of only two members.</li>
          <li>No entries without registration.</li>
          <li>
            Participants (Diploma/UG/PG students) are allowed from outside OPJU.
          </li>
          <li>Participants should not bring any pre-cooked food.</li>
          <li>
            Cooking should be done within the time limit (intimated on the same
            day).
          </li>
          <li>
            Participants should bring their own items required for plating and
            decoration (flowers, fruits, veggies etc.).
          </li>
          <li>
            Winners (declared on the same day) will be selected by judges.
          </li>
          <li>Participants should bring their own white aprons.</li>
        </ul>
      </div>

      <!-- rounds of event -->
      <div class="detail-judg">
        <h2>{{ 'Rounds of the event'.toUpperCase() }}</h2>
        <p>
          <b>1st Round:</b> Your dish with our ingredients. <br />
          <b>2nd Round:</b> Our dish with our ingredients. <br /><br />
          <b
            >After the completion of first round, the highest scoring
            competitors will enter in the second round.</b
          >
        </p>
      </div>

      <!-- note-->
      <div class="detail-judg">
        <p>
          <b>Note:</b> <br />
          1. A quiz competition (related to dish, nutritional level and hygiene)
          will be held during the cooking period. Teams who will give more
          correct answers will get extra ingredients for their recipes. <br />
          2. In the 2nd round participants will pick one anonymous note of
          recipes and cook accordingly in given time.
        </p>
      </div>

      <!-- Judgemental Criteria -->
      <div class="detail-judg">
        <h2>{{ 'Judgemental Criteria'.toUpperCase() }}</h2>
        <ul>
          <li>Taste</li>
          <li>Presentation</li>
          <li>Cleanliness and Hygiene</li>
          <li>Creativity</li>
          <li>Minimum wastage of food materials</li>
        </ul>
        <p>
          Note <br />
          1. Each parameter contains 10 marks.<br />
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
              src="/prize-other2.png"
              format="webp"
              width="130"
              height="130"
            />
            <span>3 Consolation Prize</span>
          </li>
          <li class="prize">
            <nuxt-img
              src="/certificate.png"
              format="webp"
              width="90"
              height="90"
            />
            <span style="text-align: center"
              >Certificate of appreciation<br />for all the participants</span
            >
          </li>
        </ul>
      </div>

      <!-- venue -->

      <div class="detail-judg">
        <h2>{{ 'venue'.toUpperCase() }}</h2>
        <p>
          <b>Cafeteria ground floor (next to Hub G-05).</b>
        </p>
      </div>

      <!-- contact details -->
      <div class="detail-contact">
        <h2>{{ 'Contact details'.toUpperCase() }}</h2>
        <event-details :teams="event.teams" />
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
        img: 'foodfiesta.jpg',
        event_desc:
          'Cooking is all about people. Food has a power to bring everyone together by exchanging the tastes, traditions, and cultures. OPJU brings an extraordinary platform to the students “FOOD FIESTA” to showcase their culinary knowledge and cooking skills. ',
        teams: [
          { img: 'ayushgupta.jpg', name: 'Ayush Gupta', call: '7869108678' },
          {
            img: 'vaibhavgupta.jpg',
            name: 'Vaibhav Gupta',
            call: '8827902201',
          },
          {
            img: 'amnesh.jpg',
            name: 'Amnesh Ranjan Tiwari',
            call: '7000957608',
          },
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
