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
            <li>Magic</li>
            <li>Story telling</li>
            <li>Mimicry</li>
            <li>Poetry</li>
            <li>Mime</li>
            <li>Gymnastics</li>
            <li>Standup comedy</li>
          </ul>
          <ul class="ms-1">
            <li>5 min speed painting</li>
            <li>Toss juggling</li>
            <li>Shadow act</li>
            <li>Beat boxing</li>
            <li>Sand art</li>
            <li>Instrument play</li>
          </ul>
        </div>
      </div>

      <!-- event theme -->
      <div class="detail-rules">
        <h2>{{ 'theme'.toUpperCase() }}</h2>
        <p>Glorify yourself through your talent & creativity</p>
      </div>

      <!-- event rules and regulation -->
      <div class="detail-rules">
        <h2>{{ 'Rules and Regulation'.toUpperCase() }}</h2>
        <ul>
          <li>It is an individual event i.e. one entry per registration.</li>
          <li>
            Registrations are allowed in one category per individual only.
          </li>
          <li>
            Performance should be within the time limit which will be intimated
            later.
          </li>
          <li>Performers should bring their own props.</li>
          <li>
            Contents should not be offensive, politically driven, gender biased,
            personal comments or any sensitive topic.
          </li>
          <li>No abusive language.</li>
          <li>Costumes should be appropriate.</li>
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
      </div>

      <!-- Judgemental Criteria -->
      <div class="detail-judg">
        <h2>{{ 'Judgemental Criteria'.toUpperCase() }}</h2>
        <ul>
          <li>Clarity in performance</li>
          <li>Originality</li>
          <li>Confidence</li>
          <li>Message conveyed</li>
        </ul>
      </div>

      <!-- notes -->
      <div class="detail-judg">
        <h2>{{ 'note'.toUpperCase() }}</h2>
        <ul>
          <li>Each parameter contains 10 marks.</li>
          <li>Initial round will be judged by in-house faculty.</li>
          <li>
            Final round will be judged by External judges as well as in-house
            faculty.
          </li>
          <li>
            The parameter of judgement may change which will be intimated later.
          </li>
        </ul>
      </div>

      <!-- prizes -->
      <div class="detail-judg">
        <h2>{{ 'prizes'.toUpperCase() }}</h2>
        <p>
          1. First, Second and Third <br />
          2. Certificate of appreciation for all the participants.
        </p>
      </div>

      <!-- venue -->
      <div class="detail-judg">
        <h2>{{ 'venue'.toUpperCase() }}</h2>
        <p>
          <b>
            Any open space preferably nearby babuji's statue or open air theatre
            (to be notified later).
          </b>
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
  name: 'TalentHuntEventPage',
  data() {
    return {
      event: {
        name: 'Talent Hunt - (Talent hits a target; no one else can hit)',
        img: 'talenthunt.png',
        event_desc:
          'OPJU brings you the platform of TALENT HUNT to showcase your talents and let the world celebrate your identity.',
        teams: [
          {
            img: 'suhani.jpg',
            name: 'Suhani Agrawal',
            call: '9685026258',
            mail: 'suha.bsc21ma12@opju.ac.in',
          },
          {
            img: 'mimansa.png',
            name: 'Mimansa Kashyap',
            call: '9399175434',
            mail: 'mima.mba2127@opju.ac.in',
          },
          {
            img: 'jayant.jpg',
            name: 'Jayant Shekhar Singh',
            call: '9123147552',
            mail: 'jaya.bt21me23@opju.ac.in',
          },
          {
            img: 'siddhika.jpg',
            name: 'Siddhika Modi',
            call: '7223831160',
            mail: 'sidd.bba2183@opju.ac.in',
          },
          {
            img: 'shubhjeet.jpg',
            name: 'Shubhjeet Chawla',
            call: '8269994015',
            mail: 'sidd.bba2183@opju.ac.in',
          },
          {
            img: 'divyansh.jpg',
            name: 'Divyansh Sharma',
            call: '7223043576',
            mail: 'sidd.bba2183@opju.ac.in',
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
