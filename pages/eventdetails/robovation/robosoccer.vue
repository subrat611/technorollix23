<template>
  <div class="event-details-wrapper">
    <back-btn />
    <div class="detail-container">
      <!-- img -->
      <div class="detail-img">
        <nuxt-img :src="'/event/' + event.img" />
        <div class="overlay"></div>
      </div>

      <!-- Robo soccer -->
      <!-- header -->
      <div class="detail-header">
        <!-- header -->
        <div class="header-one">
          <h1>{{ event.name_of_event_two.toUpperCase() }}</h1>
          <div class="detail-info">
            <p>{{ event.event_two_desc }}</p>
          </div>
        </div>
      </div>

      <!-- event theme -->
      <div class="detail-rules">
        <h2>{{ 'theme'.toUpperCase() }}</h2>
        <p>One Team. One Robot. Limitless Possibilities.</p>
      </div>

      <!-- overview -->
      <div class="detail-judg">
        <h2>RULES AND ROUND OF THE ROBO SOCCER</h2>
        <div class="detail-info">
          <h2>COMPETITION OVERVIEW</h2>
          <p style="background: none; border: none">
            Robo soccer is one of famous challenges of robovation in this event
            teams comes with single robot and chase ball around the big size of
            arena with the aim to kick more goals than the opponent these games
            give opportunity to youngsters to solve robotic challenges, built
            creative bots while learning engineering technology. the most
            rewarding part of designing bots is that student have fun, work
            together as a team and robot specially design for robo soccer match.
            the event is aimed at testing the flipping, kicking manueuvering
            skills and the control of the robot. The event mainly consists of
            <b>ROUND 1 AND ROUND 2</b>.
          </p>
        </div>
      </div>

      <!-- ROUND 1(ELIMINATION) -->
      <div class="detail-round-one">
        <h2>ROUND 1 (ELIMINATION)</h2>
        <ul>
          <li>
            3 balls are placed at specified locations on the arena and 5 teams
            allowed to enter in the arena.
          </li>
          <li>Only selected 2 teams who scoring high goals.</li>
          <li>Time limit is 5 minutes.</li>
          <li>
            Participants can drive, push or hit the ball into any of the goal
            posts (only two goal post).
          </li>
          <li>Points = number of goals.</li>
          <li>
            If the ball is hit out of the arena, then it will not be placed
            back.
          </li>
        </ul>
      </div>

      <!-- Round 2 -->
      <div class="detail-round-two">
        <h2>ROUND 2</h2>
        <ul>
          <li>
            Only one ball will be placed at the centre, robots are initially
            placed at their respective goal posts.
          </li>
          <li>Time limit is 5 minutes.</li>
          <li>1 no of goals = 5 points.</li>
          <li>
            Participants should hit the ball into the opponent's goal to score
            points.
          </li>
          <li>
            Each participant can make as many as goals in the limited time.
          </li>
          <li>
            Robot gets negative points (2 points) each time when its
            intentionally hits the opponent robot.
          </li>
          <li>
            If ball gets hits out of the arena, then penalty shot will be given
            to opponent team (Opponent team will heat the ball from where the
            ball was hits out of the arena). And second team will defend its
            goal.<br />
            <b>
              Judging criteria for final winner will be based on number of goals
              scored and time taken. </b
            >.
          </li>
        </ul>
      </div>

      <!-- ROBOT SPECIFICATIONS: -->
      <div class="detail-spec">
        <h2>ROBOT SPECIFICATIONS</h2>
        <ul>
          <li>The robot should fit inside a box of 30cm*30cm*20cm.</li>
          <li>Robot should not exceed 3 kg.</li>
          <li>The robot can be, wireless.</li>
          <li>
            The robot should be self-powered with supply not exceeding 12V (on
            board powersupply).
          </li>
          <li>
            Power supply (only DC) is allowed. Participants cannot draw power
            from outside main(220v) power supply.
          </li>
          <li>
            Only one participant should control the robot No player can be
            exchanged in the match.
          </li>
        </ul>
      </div>

      <!-- RULES AND REGULATIONS: -->
      <div class="detail-rules">
        <h2>RULES AND REGULATIONS</h2>
        <ul>
          <li>Team can have maximum number of four members.</li>
          <li>
            Only one participant should control the robot and one for holding
            battery or wire. No player can be exchanged in the middle of match.
          </li>
          <li>
            A robot can push or hit the ball. It cannot withhold or grab the
            ball.
          </li>
          <li>Motor should be 200rpm to 300rpm.</li>
          <li>
            Human interference (e.g., touching the robot) during the game is not
            allowed.
          </li>
          <li>
            If there is any technical issue in robot a technical time out will
            be given for 2 minutes.
          </li>
          <li>
            Decision of the Judges and Event Organizers shall be treated as
            final and binding on all and cannot be contested.
          </li>
          <li>
            The event coordinator is the match referee. He takes all the
            decisions and participants have to abide by it.
          </li>
          <li>
            No more AC/DC power supply will be provided at the sight of play.
          </li>
          <li>
            Coordinators reserve the right to ask for the explanation of the
            robot. The coordinator can change the rules of the game depending on
            the situation.
          </li>
          <li>
            Rules & Regulations may change without prior notice, by the Event
            organizers.
          </li>
          <li>
            Positions of balls will be decided by the organizers on the
            particular day of event.
          </li>
          <li>The robot is wireless or autonomous.</li>
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
          <b>Babuji Chauk</b>
        </p>
      </div>

      <!-- contact -->
      <div class="detail-contact">
        <h2>EVENT MANAGER</h2>
        <event-details :teams="event.teams" />
      </div>

      <!-- robo soccer -->
    </div>
  </div>
</template>

<script>
export default {
  name: 'RoboSoccerEventPage',
  data() {
    return {
      event: {
        name: 'robovation',
        img: 'robo-soccor.jpg',
        name_of_event_two: 'Robo Soccer',
        event_two_desc:
          'Robo soccer is one of famous challenges of robovation in this event teams comes with single robot and chase ball around the big size of arena with the aim to kick more goals than the opponent.',
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
