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
        <p>Back to school - Hip-Hop | Heavy Metal | Rock</p>
      </div>

      <!-- event rules and regulation -->
      <div class="detail-rules">
        <h2>{{ 'Rules and Regulation'.toUpperCase() }}</h2>
        <ul>
          <li>
            Team Size <br />
            Minimum - 02 <br />
            Maximum - 10
          </li>
          <li>
            Program Rounds and Time Limits:
            <p>Audition/Preliminary Round 10 minutes</p>
            <p>Semi-Final Round 15 minutes</p>
            <p>
              For the final round 3 teams to be shortlisted for a performance of
              20 minutes.
            </p>
          </li>
          <li>
            Competitors will be evaluated on technique, musicianship, and
            overall presentation. Judge's comments will not be made available to
            competitors until after the final round of the competition.
            Competitors are encouraged to inquire for comments directly from the
            judges only after the competition has ended. Upon such requests,
            sharing comments with performers is at the sole discretion of each
            judge.
          </li>
          <li>
            Choice of music is entirely at the discretion of the competitor. A
            competitor may perform the same or different music from round to
            round without penalty.
          </li>
          <li>
            It is expected that each competitor's choice of music fits within
            the time allowed for each round. Timing begins with the first note
            of the performance and continues between pieces. If a competitor
            exceeds the given time allotted, that competitor will be asked to
            stop but at no penalty to his or her evaluation.
          </li>
          <li>All judge's decisions are final.</li>
          <li>
            By participating in the final round of the competition all
            performers agree to terms allowing the University competition to use
            audio and video recording of their final-round performance for
            archival and promotional purposes.
          </li>
        </ul>
      </div>

      <!-- Judgemental Criteria -->
      <div class="detail-judg">
        <h2>{{ 'Judgemental Criteria'.toUpperCase() }}</h2>
        <p>
          <b
            >The winner is determined by a panel of judges, or by a voice vote
            of the audience or the band who brings the most people to support
            them, or in a combination of the aforementioned criteria.</b
          >
        </p>
      </div>

      <!-- venue -->

      <div class="detail-judg">
        <h2>{{ 'venue'.toUpperCase() }}</h2>
        <p>
          <b>Open Theatre in the campus of OP Jindal University.</b>
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
  name: 'BattleOfBandsEventPage',
  data() {
    return {
      event: {
        name: 'Battle of bands',
        img: '',
        event_desc:
          "Battle of Bands is a competition between musical bands to show their talent and compete against each other. It's designed to bring college students together and inspire creativity, ingenuity, and personal growth through music. For the event, bands are given time slots to perform on stage. After the performance, judges score each band on criteria such as musicality and stage presence. ",
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
