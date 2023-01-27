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
        <p>Online shooting and strategical game.</p>
      </div>

      <!-- code Of Conduct For Lan Gaming 2022 -->
      <div class="detail-rules">
        <h2>Code Of Conduct For Lan Gaming 2022</h2>
        <div class="flex justify-content-start">
          <ul>
            <li>
              Each tournament has a ruleset that cannot be changed or modified.
              Any changes made by Victory Up can only happen after a tournament
              is finished. Users cannot ask for changes to the rules while a
              tournament is ongoing, and they are a participant.
            </li>
            <li>
              Times are set for tournaments and we ask you to not have a
              practice games against another participant in any given
              tournament, inside the tournament window. This can cause
              complications when results are sent in.
            </li>
            <li>
              We ask all users who enter our tournaments to make sure they will
              be available during said tournament. If you know that you cannot
              make a tournament, during the given times stated on the tournament
              card, we ask you to refrain from entering the tournament.
            </li>
            <li>
              Cheating is not permitted in any form, that will advantage
              yourself or any participant using Lan Gaming 2022 website or other
              properties. Any competitor or participant found cheating may be
              disqualified immediately.
            </li>
            <li>
              The obligation to behave in a professional and sportsmanlike
              manner includes an obligation on the part of Players and Team
              Managers to arrive on time and ready to complete for all games,
              matches and tournaments. It also prohibits forfeiting a game or
              match without reasonable cause.
            </li>
            <li>
              While participating in anyone of our tournaments, online or
              offline, users will conduct themselves properly in accordance with
              our rules and regulations.
            </li>
            <li>
              Be a good winner It's a great feeling to win a game or a contest,
              and you should enjoy that feeling! But at the same time, don't rub
              your opponent's nose in it. Think about the frustration you feel
              when nothing works and a game ends in defeat - in that situation,
              taunting can be tough to take.
            </li>
            <li>
              Show empathy If you are angry, try to control it before directing
              your anger at another player. There are no rights and wrongs when
              it comes to feelings, and you will experience both anger and joy
              when playing. However, there are rights and wrongs when it comes
              to how emotions such as anger are expressed - think about how it
              feels when another player takes their anger out on you. One rule
              to remember is to treat people the same way online as you would
              offline.
            </li>
            <li>
              If you are angry at a loss, do not take it out on your teammates
              or find ways to pass the blame - try instead to look at the
              statistics or the replay and consider how you could have played
              differently.
            </li>
          </ul>
        </div>
      </div>

      <!-- rounds -->
      <div class="detail-judg">
        <h2>{{ 'rounds'.toUpperCase() }}</h2>
        <p><b>Knockout rounds will be conducted.</b></p>
      </div>

      <!-- prizes -->
      <div class="detail-judg">
        <h2>{{ 'prizes'.toUpperCase() }}</h2>
        <p>
          1. 1st prize - ₹5000 <br />
          2. 2nd prize - ₹3000 <br />
          3. Best duelist - ₹1000 <br />
          4. Best initiater - ₹1000 <br />
          5. Best sentinel - ₹1000 <br />
          6. Best controller - ₹1000 <br />
        </p>
      </div>

      <!-- venue -->
      <div class="detail-judg">
        <h2>{{ 'venue'.toUpperCase() }}</h2>
        <p>
          <b>C++ Lab</b> <br />
          <b>C Lab 11</b>
        </p>
      </div>

      <!--  -->
      <div class="detail-judg">
        <h2>{{ 'requirements from college'.toUpperCase() }}</h2>
        <ul>
          <li>LAN Cables</li>
          <li>Wi-Fi</li>
          <li>Tables</li>
        </ul>
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
  name: 'LanGamingEventPage',
  data() {
    return {
      event: {
        name: 'LAN GAMING',
        img: 'langaming.jpg',
        event_desc:
          'OPJU brings you the platform of LAN Gaming  Valorant 2023: Valorant is a 5v5 online shooting and strategical game.',
        teams: [
          {
            img: 'ritikprasad.png',
            name: 'Ritik Prasad',
            call: '7479882167',
            mail: 'riti.btl22cs07@opju.ac.in',
          },
          { img: '', name: 'Kunal Joshi', call: '6371104362' },
          { img: '', name: 'Atul Kumar Singh', call: '9755305060' },
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
