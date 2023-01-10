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
          <p>{{ event.event_one_desc }}</p>
        </div>

        <h2>RULES AND ROUND OF THE ROBO RACE</h2>
      </div>

      <!-- info -->
      <div class="detail-info">
        <p>
          Design a robot wire or wireless within the specified dimensions that
          can operated manually and can travel through all turns of the track.
          The robot that will complete the specified task in least time will be
          the winner. and not allowed to skip any obstacles or hurdles.
        </p>
      </div>

      <!-- spec -->
      <div class="detail-spec">
        <h2>ROBOT SPECIFICATIONS</h2>
        <ul>
          <li>
            The maximum dimension of the robot can be 30cm x 30cm x20 cm (l x b
            x h).
          </li>
          <li>The robot may be wired and wireless.</li>
          <li>Motor rpm specification 200rpm to 300 rpm.</li>
          <li>Maximum weight must not exceed 3 kg.</li>
          <li>
            The participants will have to provide power supply on board (no
            additional power supply is accepted).
          </li>
          <li>
            The machine must not be made from Lego parts, or any ready-made kit,
            if we find such machine it will be disqualified.
          </li>
          <li>
            The length of the wire (for wired bots) should be long enough to
            cover the whole track and should remain slack during the complete
            run.
          </li>
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
            The robot will be judged on basis of (in priority): - A Time to
            complete the track. b). Number of checkpoints cleared.
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
            The length of the wire (for wired bots) should be long enough to
            cover the whole track and wire should remain slack during the
            complete run.
          </li>
        </ul>
      </div>

      <!-- contact -->
      <div class="detail-contact">
        <h2>EVENT MANAGER</h2>
      </div>

      <!-- Robo soccer -->
      <!-- header -->
      <div class="detail-header">
        <!-- header -->
        <div class="header-one">
          <h1>{{ event.name_of_event_two.toUpperCase() }}</h1>
          <p>{{ event.event_two_desc }}</p>
        </div>

        <h2>RULES AND ROUND OF THE ROBO SOCCER</h2>
      </div>

      <!-- overview -->
      <div class="detail-overview">
        <h2>COMPETITION OVERVIEW</h2>
        <p>
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

      <!-- ROUND 1(ELIMINATION) -->
      <div class="detail-round-one">
        <h2>ROUND 1 (ELIMINATION)</h2>
        <ul>
          <li>
            3 balls are placed at specified locations on the arena and 5 teams
            allowed to enter in the arena.
          </li>
          <li>only Selected 2 teams who scoring high goals.</li>
          <li>Time limit is 5 minutes.</li>
          <li>
            Participants can drive, push or hit the ball into any of the goal
            posts (only two goal post)
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
            Participants should hit the ball into the opponent’s goal to score
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
            goal. <br />
            <b>
              Judging criteria for final winner will be based on number of goals
              scored and time taken </b
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
          <li>The robot can be wired, wireless.</li>
          <li>
            The robot should be self-powered with supply not exceeding 12V (on
            board powersupply).
          </li>
          <li>
            Power supply (only DC) is allowed. Participants cannot draw power
            fromoutside main(220v) power supply.
          </li>
          <li>
            Only one participant should control the robot and one for holding
            battery or wire. No player can be exchanged in the match.
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
            final and binding on all and cannot becontested.
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
          <li>
            The length of the wire (for wired bots) should be long enough and
            you cannot drag the wire during hitting the ball, wire should remain
            slack during the event.
          </li>
        </ul>
      </div>

      <!-- contact -->
      <div class="detail-contact">
        <h2>EVENT MANAGER</h2>
      </div>

      <!-- robo soccer -->
    </div>
  </div>
</template>

<script>
export default {
  name: 'RobovationEventPage',
  data() {
    return {
      event: {
        name: 'robovation',
        img: 'robovation.jpg',
        name_of_event_one: 'Robo Race',
        event_one_desc:
          'Design a wired/wireless manually controlled robot which should be able to travel on all the hurdles and complete the track in minimum amount of time.',
        name_of_event_two: 'Robo Soccer',
        event_two_desc:
          'Robo soccer is one of famous challenges of robovation in this event teams comes with single robot and chase ball around the big size of arena with the aim to kick more goals than the opponent.',
      },
    }
  },
}
</script>

<style lang="scss" scoped>
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
