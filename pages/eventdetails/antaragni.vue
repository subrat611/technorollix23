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
        <h2>You can apply in any of the following categories</h2>
        <div class="flex justify-content-start">
          <ul>
            <li>Dance (Solo and group)</li>
            <li>Singing</li>
            <li>Rap Battle</li>
            <li>Short Film Making</li>
            <li>Fusion</li>
          </ul>
        </div>
      </div>

      <!-- event theme -->
      <div class="detail-rules">
        <h2>{{ 'theme'.toUpperCase() }}</h2>
        <p>The Fire Within</p>
      </div>

      <!-- event rules and regulation -->
      <div class="detail-rules">
        <h2>{{ 'Rules of the event'.toUpperCase() }}</h2>
        <ul>
          <li>Inappropriate (vulgar) songs are not permitted for the dance.</li>
          <li>
            Every contestant should provide their tracks to the coordinators in
            advance for the smooth conduction of the event.
          </li>
          <li>
            Overall judgement will be based upon performance, decency,
            discipline of contestants.
          </li>
          <li>Performers should bring their own props</li>
          <li>
            Contents should not be offensive, politically driven, gender biased,
            personal comments or any sensitive topic.
          </li>
          <li>Costumes should be appropriate.</li>
          <li>No entries without registration.</li>
          <li>Decision of the jury will be final.</li>
          <li>
            The contestants should strictly follow all the rules and regulations
            of the event.
          </li>
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
      </div>

      <!-- Judgemental Criteria -->
      <div class="detail-judg">
        <h2>{{ 'Judgemental Criteria'.toUpperCase() }}</h2>
        <ul>
          <li>
            For singing, judgement will be based upon voice quality, music,
            nodes, pitch, stage presentation, synchronization.
          </li>
          <li>Theme</li>
          <li>Energy level</li>
          <li>Clarity in performance</li>
          <li>Confidence</li>
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
              src="/certificate.png"
              format="webp"
              width="130"
              height="130"
            />
            <span style="text-align: center"
              >Certificate of appreciation<br />
              for all the participants.</span
            >
          </li>
        </ul>
      </div>

      <!-- venue -->

      <div class="detail-judg">
        <h2>{{ 'venue'.toUpperCase() }}</h2>
        <p>
          <b>Multi Purpose Hall and campus ground</b>
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
  name: 'AntaragniEventPage',
  data() {
    return {
      event: {
        name: 'ANTARAGNI - GRAND-E-ROLLIX',
        img: 'antaragni.jpg',
        event_desc:
          'ANTARAGNI  has been known for incorporating cultural excellence and opportunities.',
        teams: [
          {
            img: 'ankit.jpg',
            name: 'Ankit Patnayak',
            call: '6232518588',
            mail: 'anki.ug20cse06@opju.ac.in',
          },
          {
            img: 'rishikabansal.jpg',
            name: 'Rishika Bansal',
            call: '7030630729',
            mail: 'rish.ug20bscma12@opju.ac.in',
          },
          {
            img: 'krashika.jpg',
            name: 'Krashika Shukla',
            call: '8269118713',
            mail: 'kras.bsc21ma06@opju.ac.in',
          },
          {
            img: 'taslimatandi.jpg',
            name: 'Taslima Tandi',
            call: '9337974219',
            mail: 'tanditaslima@gmail.com',
          },
          {
            img: 'suraj.jpg',
            name: 'Suraj Gupta',
            call: '8770299558',
            mail: 'surajam2002@gmail.com',
          },
          {
            img: 'shurutisingh.jpg',
            name: 'Shuruti Singh',
            call: '9770376585',
            mail: 'shur.ug20cse47@opju.ac.in',
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
