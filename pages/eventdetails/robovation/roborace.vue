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
        <!-- header -->
        <div class="header-one">
          <h1>{{ event.name_of_event_one.toUpperCase() }}</h1>
          <div class="detail-info">
            <p>{{ event.event_one_desc }}</p>
          </div>
        </div>
      </div>

      <!-- event theme -->
      <div class="detail-rules">
        <h2>{{ 'theme'.toUpperCase() }}</h2>
        <p>One Team. One Robot. Limitless Possibilities.</p>
      </div>

      <!-- info -->
      <div class="detail-judg">
        <h2>RULES AND ROUND OF THE ROBO RACE</h2>
        <div>
          <p>
            Design a wireless control robot with specified dimensions that can
            operate autonomously and travel through all track turns. The robot
            that will complete the specified task in the least time will be the
            winner and will not be allowed to skip any obstacles or hurdles.
          </p>
        </div>
      </div>

      <!-- spec -->
      <div class="detail-spec">
        <h2>ROBOT SPECIFICATIONS</h2>
        <ul>
          <li>
            The maximum dimension of the robot can be 30cm x 30cm x20 cm (l x b
            x h).
          </li>
          <li>The robot may be and wireless.</li>
          <li>Motor rpm specification 200rpm to 300 rpm.</li>
          <li>Maximum weight must not exceed 3 kg.</li>
          <li>
            The participants will have to provide power supply on board (no
            additional power supply is accepted).
          </li>
          <li>
            The machine must not be made from Lego parts or any ready-made kit,
            if we find such machine that will be disqualified.
          </li>
          <li>The robot should be wireless.</li>
        </ul>
      </div>

      <!-- BATTERIES & POWER: -->
      <div class="detail-power">
        <h2>BATTERIES & POWER</h2>
        <ul>
          <li>The bots must be powered electrically only.</li>
          <li>
            Batteries must be sealed, immobilized electrolyte type (lithium,
            NiCad, or dry cells).
          </li>
          <li>
            The electric voltage anywhere in the bot should not be more then 12V
            DC at any point of time.
          </li>
        </ul>
      </div>

      <!-- general rules -->
      <div class="detail-rules">
        <h2>GENERAL RULES</h2>
        <ul>
          <li>
            This is racing event so fastest and most balanced robot will win.
          </li>
          <li>Robot should be as per the given specifications.</li>
          <li>Each team can have maximum Four members.</li>
          <li>Students from different institutes can form a team.</li>
          <li>
            Each member of the team must contain the identity card of his/her
            respected institute.
          </li>
          <li>The robot should not damage the arena.</li>
          <li>No test practice will be allowed on the arena.</li>
          <li>
            The robot must not leave behind any of its parts during the run;
            else it will result in disqualification.
          </li>
          <li>
            Unethical behaviour could lead to disqualification. Faculty
            co-ordinators have all the rights to take final decision for any
            matter during the event. and Judge's decision will be considered
            final.
          </li>
          <li>
            Certificates of Participation will be given to all the teams that
            will participate in the event, but not to the teams which get
            disqualified due to disobeying any of the competition rules.
            *Co-ordination committee reserves the right to add or update any
            rule.
          </li>
        </ul>
      </div>

      <!-- track spec -->
      <div class="detail-track">
        <h2>TRACK SPECIFICATION</h2>
        <p>The length of Track will be approximately 28 meters.</p>
        <p>
          <b>
            SAND AND STONE, RUMBLE STRIPS, WATER SPRINKER, SMALL HOLES COVERED
            ALL SIDE, SWITCH BRIDGE, SPEED BRAKERS, SLIPPERY AND MANY MORE.
          </b>
        </p>
      </div>

      <!-- game rule -->
      <div class="detail-game-rules">
        <h2>GAME RULE</h2>
        <ul>
          <li>
            The competition is based on time trail system. There will a
            qualifying round for each team.
          </li>
          <li>
            The top team from qualifying round makes it to the final round on
            basis of time trials.
          </li>
          <li>
            If any of the robots starts off before start up call, the counter
            would be restarted and the machines will get a second chance. If
            repeated again then team will be disqualified.
          </li>
          <li>Your robot must be ready when call is made for your team.</li>
          <li>
            Team members will be allowed only four times to touch or reset their
            robots position during the run. However, this will lead to a time
            penalty and timer will not stop during this course of action.
          </li>
          <li>
            The robot will be judged on basis of (in priority): - <br />
            (a) A Time to complete the track.<br />
            (b) Number of checkpoints cleared.
          </li>
          <li>
            Must not contain any readymade kits, pneumatic &hydraulic systems,
            IC engines.
          </li>
          <li>Decision about your robot will be taken by the organizers.</li>
          <li>
            No team will get a second chance after completing the track with
            poor score.
          </li>
          <li>
            The length of the wire (for bots) should be long enough to cover the
            whole track and wire should remain slack during the complete run.
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
            <span>Rs. 5000</span>
          </li>
          <li class="prize">
            <nuxt-img
              src="/prize2.png"
              format="webp"
              width="130"
              height="130"
            />
            <span>Rs. 3000</span>
          </li>
          <li class="prize">
            <nuxt-img
              src="/prize3.png"
              format="webp"
              width="130"
              height="130"
            />
            <span>Rs. 2000</span>
          </li>
        </ul>
      </div>

      <!-- venue -->

      <div class="detail-judg">
        <h2>{{ 'venue'.toUpperCase() }}</h2>
        <p>
          <b>Basketball Ground</b>
        </p>
      </div>

      <!-- contact -->
      <div class="detail-contact">
        <h2>EVENT MANAGER</h2>
        <event-details :teams="event.teams" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'RoboRaceEventPage',
  data() {
    return {
      event: {
        name: 'robovation',
        img: 'robo-race.jpg',
        name_of_event_one: 'Robo Race',
        event_one_desc:
          'Design a wireless or Bluetooth controlled robot which should be able to travel on all the hurdles and complete the track in minimum amount of time.',
        teams: [
          {
            img: 'rishav.jpeg',
            name: 'Rishav kumar',
            call: '9580542886',
            mail: 'rishabhkumarbasketball7573@gmail.com',
          },
          {
            img: 'sushil.jpeg',
            name: 'Sushil kumar',
            call: '9113159596',
            mail: 'sush.del21me05@opju.ac.in',
          },
          {
            img: 'amankumar.jpeg',
            name: 'Aman kumar',
            call: '7070171324',
            mail: '',
          },
          {
            img: 'avin.jpg',
            name: 'Avinash singh',
            call: '7691953404',
            mail: 'avin.bt21me15@opju.ac.in',
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

      h2 {
        padding: 1rem 0;
      }

      .header-one {
        margin: 1rem 0;

        h1 {
          font-family: 'Poppins', sans-serif;
          background: -webkit-linear-gradient(#ff0084, #e3e3e3);
          background-clip: text;
          -webkit-background-clip: text;
          -webkit-text-fill-color: transparent;
        }

        h1,
        p {
          padding: 0.3rem 0;
        }

        p {
          font-size: 1.1rem;
          font-family: 'Roboto', sans-serif;
          line-height: 1.5rem;
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

    .detail-spec,
    .detail-power,
    .detail-rules,
    .detail-judg,
    .detail-game-rules,
    .detail-round-one,
    .detail-round-two {
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

    .detail-track {
      margin-top: 1.5rem;

      p {
        margin-top: 1rem;
        padding: 0.2rem 0;
        font-size: 1.1rem;
        font-family: 'Roboto', sans-serif;
        line-height: 1.6rem;
      }
    }

    .detail-contact {
      margin-top: 1.5rem;
    }

    // robo soccer
    .detail-overview {
      background: rgba(63, 194, 255, 0.11);
      border-radius: 7px;
      box-shadow: 0 4px 30px rgba(104, 104, 104, 0.1);
      backdrop-filter: blur(3.3px);
      -webkit-backdrop-filter: blur(3.3px);
      border: 1px solid rgba(255, 217, 252, 0.2);
      padding: 1rem;

      h2 {
        padding: 0.2rem 0;
      }

      p {
        font-family: 'Roboto', sans-serif;
        font-size: 1.1rem;
        line-height: 1.6rem;
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
