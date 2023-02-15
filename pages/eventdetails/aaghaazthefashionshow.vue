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
        <p>RED CARPET</p>
      </div>

      <!-- event rules and regulation -->
      <div class="detail-rules">
        <h2>{{ 'Rules and Regulation'.toUpperCase() }}</h2>
        <ul>
          <li>
            All the participants should come half and hour before the show
          </li>
          <li>Students must be prepared with their attire.</li>
          <li>
            No students shall be allowed for direct participation in final
            rounds, and no students is entitled for wildcard entries except for
            students outside of OPJUS.
          </li>
          <li>No vulgarism is allowed in clothes selection.</li>
          <li>
            The score evaluation will be done based on a walk, presentation, and
            q/a round etc.
          </li>
          <li>
            Judges result will be concluded as the final result and shall be
            accepted by each and every student.
          </li>
        </ul>
      </div>

      <!-- rounds -->
      <div class="detail-judg">
        <h2>Rounds</h2>
        <ul>
          <li>1st round 80s -90s bollywood</li>
          <li>2nd and 3rd round will be declared before 2-3 days.</li>
        </ul>
      </div>
      <!-- Judgemental Criteria -->
      <div class="detail-judg">
        <h2>{{ 'Judgemental Criteria'.toUpperCase() }}</h2>
        <ul>
          <li>PERSONALITY</li>
          <li>WALK</li>
          <li>QUESTION\ANSWER</li>
          <li>COMMUNICATION</li>
        </ul>
      </div>

      <!-- prizes -->
      <div class="detail-judg">
        <h2>{{ 'prizes'.toUpperCase() }}</h2>
        <ul class="prize-wrapper">
          <li class="prize">
            <nuxt-img
              src="/prize-other2.png"
              format="webp"
              width="130"
              height="130"
            />
            <span>MR & MRS AAGHAAZ</span>
          </li>
        </ul>
      </div>

      <!-- venue -->
      <div class="detail-judg">
        <h2>{{ 'venue'.toUpperCase() }}</h2>
        <p>IN FRONT OF CHEMISTRY LAB (ROUND 1 & ROUND 2)</p>
      </div>

      <!-- contact details -->
      <div class="detail-contact">
        <h2>{{ 'Contact details'.toUpperCase() }}</h2>
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
  name: 'AaghaazEventPage',
  data() {
    return {
      event: {
        name: 'Aaghaaz the fashion show',
        img: 'aaghaaz.png',
        event_desc:
          "The fashion it's a form of self-expression and autonomy at a particular period and place and in a specific context of  clothing, footwear, lifestyles , accessories , makeup, hairstyles and body posture.",
        team: [
          {
            img: '',
            name: 'Rahul Shrivas',
            call: '7770881289',
          },
          {
            img: '',
            name: 'Parth Singh Thakur',
            call: '8889055521',
          },
          {
            img: '',
            name: 'Shubhangi  Bohidar',
            call: '6260226147',
          },
          {
            img: '',
            name: 'Anurag Sikdar',
            call: '9617663919',
          },
          {
            img: '',
            name: 'Harsh Sharma',
            call: '7389258696',
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
