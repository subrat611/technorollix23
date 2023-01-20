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
        <p>Bird view,Fish view, insect view, opju campus and Nature</p>
      </div>

      <!-- event rules and regulation -->
      <div class="detail-rules">
        <h2>{{ 'Rules of the event'.toUpperCase() }}</h2>
        <ul>
          <li>
            The event will happen in 2 round and continue for two days. i.e 1st
            round before 1st mar. and 2nd of Feb 2023.
          </li>
          <li>
            Every participant will have to submit single photo at the end of the
            day via G Form using which will be framed at the gallery.
          </li>
          <li>
            Last minute changes in the above rules, if necessary, can be made.
          </li>
        </ul>
      </div>

      <!-- rounds of event -->
      <div class="detail-judg">
        <h2>{{ 'Rounds of the event'.toUpperCase() }}</h2>
        <p>2 Rounds</p>
      </div>

      <!-- Judgemental Criteria -->
      <div class="detail-judg">
        <h2>{{ 'Judgemental Criteria'.toUpperCase() }}</h2>
        <p>Judge's marks</p>
      </div>

      <!-- venue -->
      <div class="detail-judg">
        <h2>{{ 'venue'.toUpperCase() }}</h2>
        <p>
          <b>Online</b>
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
  name: 'PhotorollixEventPage',
  data() {
    return {
      event: {
        name: 'Photorollix',
        img: '',
        event_desc:
          'Photorollix is a recreational event where in participants are welcomed to openly participate here to show their "third eye handling Skill" as it is said,The picture that you took with your camera is the imagination you want to create with the reality. It will be the hall of fame which will show different beautiful moment Captured by the photographers. It will make you to re-live amazing moments again and again.',
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
