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
        <div class="detail-info">
          <p>One Team. One Robot. Limitless Possibilities.</p>
        </div>
      </div>

      <!-- field dimension -->
      <div class="detail-round-one">
        <h2>FIELD DIMENSION</h2>
        <div class="detail-info">
          <p>
            The Battle ring is a fully enclosed 18 feet by 16 feet rectangle
            raised 1 feet off the ground. The Battle Box door is approximately
            level, Arena is open at the four side of corner.
          </p>
        </div>
      </div>

      <!-- match time limits -->
      <div class="detail-round-one">
        <h2>Match Time Limits</h2>
        <div class="detail-info">
          <p>
            Unless a Match terminates early, the Match will last for 3 minutes
            of fighting time. The time limit does not include any time elapsed
            as a result of Timeouts.
          </p>
        </div>
      </div>

      <!-- Early Termination -->
      <div class="detail-round-one">
        <h2>Early Termination</h2>
        <div class="detail-info">
          <p>
            A Match can be terminated early by Forfeit, Disqualification or
            Incapacitation. Tap outs are not allowed.
          </p>
        </div>
      </div>

      <!-- THE BOT -->
      <div class="detail-round-one">
        <h2>THE BOT</h2>
        <div class="detail-info">
          <p>
            The team must build and bring one pre-constructed, autonomous or
            wireless robot whose purpose is to push, throw, Filip, hit, drag or
            otherwise move the opponent out of the battle ring within the
            maximum battle time. The following section details the rules and
            specifications regarding the robot; please be sure to read them
            carefully and refer to them as you design your robot.
          </p>
        </div>
      </div>

      <!-- ROBOT SPECIFICATIONS: -->
      <div class="detail-spec">
        <h2>ROBOT SPECIFICATIONS</h2>
        <ul>
          <li>The robot should fit inside a box of 50cm*50cm*30cm.</li>
          <li>Robot should not exceed 5 kg.</li>
          <li>Maximum 5 number of motors used.</li>
          <li>The robot is only wireless.</li>
          <li>
            The robot should be self-powered with supply not exceeding 12V (on
            board power supply).
          </li>
          <li>
            Power supply (only DC) is allowed. Participants cannot draw power
            from outside main(220v) power supply.
          </li>
          <li>
            Only one participant should control the robot and No player can be
            exchanged in the match.
          </li>
        </ul>
      </div>

      <!-- Duties -->
      <div class="detail-spec">
        <h2>Duties</h2>
        <ul>
          <li>The captain asks the referee for timeouts if necessary.</li>
          <li>The bot handler can substitute a bot during match play.</li>
          <li>
            The bot handler asks the referee for the permission to substitute a
            bot in the next stoppage and, if the referee agrees, substitutes the
            bot.
          </li>
        </ul>
      </div>

      <!-- RULES AND REGULATIONS: -->
      <div class="detail-rules">
        <h2>RULES AND REGULATIONS</h2>
        <ul>
          <li>Team can have maximum number of four members.</li>
          <li>
            Only one participant should control the robot and No player can be
            exchanged in the middle of match.
          </li>
          <li>
            A robot can push or hit the opponent and move out of the ring.
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
            The event coordinator and manager and others are the match referee.
            He takes all the decisions and participants have to abide by it.
          </li>
          <li>
            No more AC/DC power supply will be provided at the sight of play.
          </li>
          <li>
            Coordinators and manager reserve the right to ask for the
            explanation of the robot. The coordinator and manager can change the
            rules of the game depending on the situation.
          </li>
          <li>
            Rules & Regulations may change without prior notice, by the Event
            organizers.
          </li>
        </ul>
      </div>

      <!-- GAME RULE JUDGEMENT CRITERIA -->
      <div class="detail-round-one">
        <h2>GAME RULE JUDGEMENT CRITERIA</h2>
        <ul>
          <li>
            The competition is based on time system. There will a qualifying
            round for each team.
          </li>
          <li>
            The top team from qualifying round will make it to the final round
            on basis of no of times it moved out opponent from the ring.
          </li>
          <li>
            If any of the robots starts off before start up call, the counter
            would be restarted and the BOT will get a second chance. If repeated
            again then team will be disqualified.
          </li>
          <li>Your robot must be ready when call is made for your team.</li>
          <li>
            Team members will be allowed only four times to touch or reset their
            robots position during the run. However, this will lead to a time
            penalty and timer will not stop during this course of action.
          </li>
          <li>
            The robot will be judged on the basis of (in priority): - <br />
            a. The Time taken to move out the opponent from the ring. <br />
            b. No of times move out opponent from the ring.
          </li>
          <li>
            Must not contain any readymade kits, pneumatic &hydraulic systems,
            IC engines.
          </li>
          <li>Decision about your robot will be taken by the organizers.</li>
          <li>No team will get a second chance after completing the game.</li>
          <li>The robot is wireless or Autonomous.</li>
          <li>
            Certificates of Participation will be given to all the teams that
            will participate in the event, but not to the teams which get
            disqualified due to disobeying any of the competition rules.
            *Co-ordination committee reserves the right to add or update any
            rule.
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

      <div class="detail-round-one">
        <h2>{{ 'venue'.toUpperCase() }}</h2>
        <div class="detail-info">
          <p><b>Babuji Chauk</b></p>
        </div>
      </div>

      <!-- contact -->
      <div class="detail-contact">
        <h2>EVENT MANAGER</h2>
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
  name: 'RoboSoccerEventPage',
  data() {
    return {
      event: {
        name: 'robovation',
        img: 'robo-war.jpg',
        name_of_event_two: 'Robo War',
        event_two_desc:
          'Robo war is the most exciting challenge of this event and main aim to move out opponent from the arena This game gives opportunity to youngsters to design, build and control combat robots to demonstrate their creativity, engineering skills and driving ability.',
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
