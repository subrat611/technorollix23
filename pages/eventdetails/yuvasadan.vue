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

      <!-- event rules and regulation -->
      <div class="detail-rules">
        <h2>{{ 'Rules and Regulation'.toUpperCase() }}</h2>
        <ul>
          <li>
            Every team has to register on the official OPJU website for the
            Yuvasadan.
          </li>
          <li>Each team must contain 3-4 members.</li>
          <li>
            There will be 2 rounds. 1st round will be the qualifying round and
            2nd round will be the final round.
          </li>
          <li>
            After all the debates are conducted in the first round, only the top
            scorer teams will be selected for the final round.
          </li>
          <li>Each team will be given the topics prior to the rounds.</li>
          <li>
            Each team will be given 2 minutes to speak about their topics and 4
            minutes will be given for the argument.
          </li>
          <li>Language could be Hindi/English.</li>
          <li>
            If, due to certain circumstances, one team could not be present
            during the debate, then that team will be disqualified.
          </li>
          <li>Participants must speak in parliamentary words only.</li>
          <li>Decision of the chairperson of the event is final.</li>
        </ul>
      </div>

      <!-- Judgemental Criteria -->
      <div class="detail-judg">
        <h2>{{ 'Judgemental Criteria'.toUpperCase() }}</h2>
        <p>
          <b
            >(Each will be containing 20 marks and total will be of 100
            marks)</b
          >
        </p>
        <ul>
          <li>
            Organization and Clarity: Viewpoints and response are outlined both
            clearly and orderly.
          </li>
          <li>Use of Arguments: Reasons given to support viewpoint.</li>
          <li>
            Use of examples and Facts: Examples and facts are given to support
            reasons, with references.
          </li>
          <li>
            Use of Rebuttal: Arguments made by the other teams are responded to
            and deal with effectively.
          </li>
          <li>
            Presentation Style: Tone of voice, use of gestures, and level of
            enthusiasm are convincing to the audience.
          </li>
        </ul>
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
              src="/prize-other.png"
              format="webp"
              width="130"
              height="130"
            />
            <span style="text-align: center">Best Punch Line</span>
          </li>
          <li class="prize">
            <nuxt-img
              src="/prize-other.png"
              format="webp"
              width="130"
              height="130"
            />
            <span style="text-align: center">Best Speaker</span>
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
  name: 'YuvaSadanEventPage',
  data() {
    return {
      event: {
        name: 'yuva sadan',
        img: 'yuva.jpg',
        event_desc:
          'The Yuvasadan, Technorollix 23, OPJU is an event to test the leadership and debating qualities of participants, stretching across different world wide issues related topics. It is not just a test of knowledge but also critical thinking skills of students. It helps you to acquire better poise, speech delivery and public speaking skills.',
        teams: [
          {
            img: 'aditi.jpeg',
            name: 'Aditi Singh',
            call: '7606909905',
          },
          {
            img: 'mousami.jpg',
            name: 'Mousami Sharma',
            call: '8260196632',
          },
          {
            img: 'palakagrawal.jpeg',
            name: 'Palak Agrawal',
            call: '8982177527',
          },
          {
            img: 'tanusingh.jpeg',
            name: 'Tanu Singh',
            call: '9179560545',
          },
          {
            img: 'yashwardhanpoddar.jpeg',
            name: 'Yashwardhan Poddar',
            call: '7440788780',
          },
          {
            img: 'sakshitiwari.jpeg',
            name: 'Sakshi Tiwari',
            call: '8602159266',
          },
          {
            img: 'pradeeprout.jpeg',
            name: 'Pardeep Rout',
            call: '9669747176',
          },
          {
            img: 'ankursingh.jpeg',
            name: 'Ankur Singh',
            call: '9031359990',
          },
          {
            img: 'shoumyasinha.jpeg',
            name: 'Shoumya Shina',
            call: '7091799799',
          },
          {
            img: 'pragatipanda.jpeg',
            name: 'Pragati Panda',
            call: '7815084095',
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
      margin-top: 4rem;
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
