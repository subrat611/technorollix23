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

      <!-- event topic (example) -->
      <div class="detail-rules">
        <h2>{{ 'Event Categories'.toUpperCase() }}</h2>
        <ul>
          <li>Working models</li>
          <li>Non-Working models</li>
          <li>Posters</li>
        </ul>
      </div>

      <!-- reason why you should participate -->
      <div class="detail-rules">
        <h2>{{ 'Reason why you should participate ?'.toUpperCase() }}</h2>
        <ul>
          <li>Exciting prizes for the winners worth ₹50,000.</li>
          <li>Funding opportunity for innovative prototypes.</li>
          <li>
            Recognization certificates for all participating Universities from
            opju innovation center.
          </li>
          <li>
            Participating Certificate will be given to all the participants.
          </li>
          <li>Special category wise winning prizes.</li>
          <li>Time to get new age experience and innovation.</li>
        </ul>
      </div>

      <!-- event rules and regulation -->
      <div class="detail-rules">
        <h2>{{ 'Rules and Regulations'.toUpperCase() }}</h2>
        <ul>
          <li>
            All the exhibits must reach the venue one hour prior to the
            prescribed time to install all the necessary components for their
            model.
          </li>
          <li>Maximum of 4 participants are allowed in each team.</li>
          <li>
            The exhibit should be a creation of the student, which either
            illustrates or demonstrates a novel cause.
          </li>
          <li>
            Exhibits must be confined to an area. Tables and Electricity
            connection will be provided.
          </li>
          <li>
            No exhibits should be dismantled or removed till the end of the
            competition
          </li>
          <li>
            Highly flammable and toxic substances are not allowed, if so
            required application has to be submitted prior .
          </li>
          <li>Every participant must maintain the decorum of the event.</li>
          <li>
            <b>External and Internal judges panel will take the final call…</b>
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
  name: 'TechLabEventPage',
  data() {
    return {
      event: {
        name: 'TechLab',
        img: 'techlab.jpg',
        event_desc:
          'Tech lab is one of the most prestigious event of Technorollix,which is the biggest tech festival of central India.The event shows the creativity and potential of bright minds from different universities through their self-developed model.',
        teams: [
          {
            img: 'soumya.png',
            name: 'Soumya Mittal',
            call: '9753721777',
          },
          {
            img: 'kraman.png',
            name: 'Kalyan Raman Korni',
            call: '6260693650',
          },
          {
            img: 'asimkumar.png',
            name: 'Asim Kumar',
            call: '9500636713',
          },
          {
            img: 'sourabh-kumar-ojha.png',
            name: 'Sourabh Kumar Ojha',
            call: '9893493205',
          },
          {
            img: 'awadesh.png',
            name: 'Awadesh Patnaik',
            call: '6260131614',
          },
          {
            img: 'anshita-mehar.png',
            name: 'Anshita Mehar',
            call: '9179184350',
          },
          {
            img: 'sandeep-singh.png',
            name: 'Sandeep Singh',
            call: '8676898925',
          },
          {
            img: 'gyanesh-bhatt.png',
            name: 'Gyanesh Bhatt',
            call: '9835594986',
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
