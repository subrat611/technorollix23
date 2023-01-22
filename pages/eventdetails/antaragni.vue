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
      <!-- <div class="detail-rules">
        <h2>You can apply in any of the following categories</h2>
        <div class="flex justify-content-start">
          <ul>
            <li>Dancing</li>
            <li>Singing</li>
            <li>Mimicry</li>
            <li>Short story telling</li>
          </ul>
          <ul class="ms-1">
            <li>Stand up comedy</li>
            <li>Drama and theater</li>
            <li>Magic show</li>
            <li>Instrument play</li>
          </ul>
        </div>
      </div> -->

      <!-- event theme -->
      <div class="detail-rules">
        <h2>{{ 'theme'.toUpperCase() }}</h2>
        <p>Kala-E-Sham</p>
      </div>

      <!-- event rules and regulation -->
      <div class="detail-rules">
        <h2>{{ 'Rules of the event'.toUpperCase() }}</h2>
        <ul>
          <li>
            Inappropriate or vulgar songs are not permitted for dancing or
            singing.
          </li>
          <li>
            Every contestant should provide their tracks to the coordinators in
            advance for the smooth conduction of the event.
          </li>
          <li>
            Overall judgment will be based on performance, decency, discipline
            of contestants.
          </li>
          <li>
            The contestants have to strictly follow all the rules and
            regulations of the event.
          </li>
          <li>
            Decision taken by the juries/faculty coordinators will be final.
          </li>
          <li>
            Only UG, PG and diploma students can participate. Students from
            outside university are eligible.
          </li>
          <li>The elimination will be done after each round by the judges.</li>
        </ul>
      </div>

      <!-- rounds of event -->
      <div class="detail-judg">
        <h2>{{ 'Rounds of the event'.toUpperCase() }}</h2>
        <p>
          There will be 3 rounds from which 2 will be conducted in MP hall and
          last round will be in the university ground at night.
        </p>
      </div>

      <!-- Judgemental Criteria -->
      <div class="detail-judg">
        <h2>{{ 'Judgemental Criteria'.toUpperCase() }}</h2>
        <ul>
          <li>
            As per judges call (voice quality, stage presentation, nodes, pitch,
            synchronization)
          </li>
        </ul>
      </div>

      <!-- prizes -->
      <div class="detail-judg">
        <h2>{{ 'prizes'.toUpperCase() }}</h2>
        <p>1. First, Second and Third<br /></p>
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
          'This event is a platform where students get to showcase their talents like dancing, singing, short film-making , rapping  and fusion etc.',
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
