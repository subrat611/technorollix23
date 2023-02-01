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
        <br />
        <p>
          Here participants throw in their propositions and present them to get
          feedback and what they should be working on or how they should advance
          regarding their ideas.
        </p>
        <br />
        <p>
          Participants work in teams and utilize design thinking and innovative
          learning practices to envision and collaborate on possible solutions.
        </p>
        <br />
        <p>
          Ideathon is not restricted to one common subject as it usually varies
          from marketing to philosophy to science.
        </p>
      </div>

      <!-- event theme -->
      <div class="detail-rules">
        <h2>{{ 'theme'.toUpperCase() }}</h2>
        <p>
          <b>Scrutinize the already scrutinized</b> <br />
          Meaning: To examine the existing things carefully to create or
          visualize something new innovatively.
        </p>
      </div>

      <!-- event topic (example) -->
      <div class="detail-rules">
        <h2>{{ 'TOPICS (FOR EXAMPLE)'.toUpperCase() }}</h2>
        <table>
          <tbody>
            <tr>
              <td>1. Impact of Workplace Diversity on Company Culture</td>
              <td>2. How Financial Literacy impacts Investment Behavior</td>
            </tr>
            <tr>
              <td>3. Environmental issues with their solution.</td>
              <td>4. Big Data and Automation in Supply Chain Management</td>
            </tr>
            <tr>
              <td>
                5. Towards a Cleaner and Greener Environment with new
                technologies
              </td>
              <td>6. Conversion of waste material into useful material.</td>
            </tr>
            <tr>
              <td>7. Agriculture, Food and Rural Development</td>
              <td>8. Block chain and Cybersecurity</td>
            </tr>
            <tr>
              <td>9. Augmented Reality</td>
              <td>10. Clean And Green Technology</td>
            </tr>
            <tr>
              <td>11. Fitness and Sports</td>
              <td>12. MedTech/BioTech/HealthTech</td>
            </tr>
            <tr>
              <td>13. Renewable/Sustainable Energy</td>
              <td>14. Robotics and Drone</td>
            </tr>
            <tr>
              <td>15. Smart Automation</td>
              <td>16. Transport and Logistics</td>
            </tr>
            <tr>
              <td>17. Disaster Management</td>
              <td>18. Big Data Technology</td>
            </tr>
            <tr>
              <td>19. Business management with AI</td>
            </tr>
          </tbody>
        </table>
      </div>

      <!-- event rules and regulation -->
      <div class="detail-rules">
        <h2>{{ 'Rules and Regulation'.toUpperCase() }}</h2>
        <ul>
          <li>
            Every participant must reach the designated venue 15 minutes before
            the event's commencement.
          </li>
          <li>
            Only registered participants are allowed to present their ideas at
            the event (Registration form will be circulated soon).
          </li>
          <li>
            An abstract must be submitted from every individual/team prior to
            the commencement of the event.
          </li>
          <li>
            The abstract must contain a brief summary of the presenter’s central
            theme/idea (maximum 400 words).
          </li>
          <li>
            Participants must have an “Innovative” solution to the existing
            problems.
          </li>
          <li>
            A participant can participate individually or in a team according to
            their willingness.
          </li>
          <li>There will be only a single round.</li>
          <li>
            Every participant's ideas will be judged on 5 different criteria.
          </li>
          <li>
            Teams/participants attaining the maximum number of points out of the
            total will be the winners.
          </li>
          <li>Each team can have a maximum of 3 participants.</li>
          <li>
            One team can submit only one idea. In case of submitting a new idea,
            the team leader must change. No team leader can present more than
            one idea.
          </li>
          <li>
            Team must have to complete their presentation within a time limit of
            08 minutes.
          </li>
          <li>
            A <i>warning bell</i> will ring at 6 minutes during the
            presentation. It will indicate the last two minutes remaining for
            the presenter to complete their presentation.
          </li>
          <li>
            After the ringing of the warning bell, the presenter must focus on
            summarizing or concluding their presentation.
          </li>
          <li>Two minutes will be given for the Query round.</li>
        </ul>
      </div>

      <!-- Judgemental Criteria -->
      <div class="detail-judg">
        <h2>{{ 'Judgemental Criteria'.toUpperCase() }}</h2>
        <p>
          <b
            >Every presenter's idea will be evaluated on 5 different criteria</b
          >
          <br />
          1. Uniqueness of the idea. <br />
          2. Feasibility of the presenter's idea. <br />
          3. Way of presentation. <br />
          4. Response to Questionnaire. <br />
          5. Scalability of the Idea
        </p>
        <p>
          Each criterion will contain a maximum of 20 points, with all the
          criteria summing up to a total of 100 points.
        </p>
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
            <span>1<sup>st</sup> Prize</span>
          </li>
          <li class="prize">
            <nuxt-img
              src="/prize2.png"
              format="webp"
              width="130"
              height="130"
            />
            <span>2<sup>nd</sup> Prize</span>
          </li>
          <li class="prize">
            <nuxt-img
              src="/prize3.png"
              format="webp"
              width="130"
              height="130"
            />
            <span>3<sup>rd</sup> Prize</span>
          </li>
          <li class="prize">
            <nuxt-img
              src="/prize-other.png"
              format="webp"
              width="130"
              height="130"
            />
            <span style="text-align: center"
              >Best Feasible<br />Idea Prize</span
            >
          </li>
          <li class="prize">
            <nuxt-img
              src="/prize-other.png"
              format="webp"
              width="130"
              height="130"
            />
            <span style="text-align: center"
              >Best Innovative Idea Prize<br />(Unique and Originality)</span
            >
          </li>
          <li class="prize">
            <nuxt-img
              src="/prize-other.png"
              format="webp"
              width="130"
              height="130"
            />
            <span>Best Presentation Prize</span>
          </li>
        </ul>
      </div>

      <!-- venue -->

      <div class="detail-judg">
        <h2>{{ 'venue'.toUpperCase() }}</h2>
        <p>
          <b>FB-14 (EEE Seminar Hall)</b> <br />
          1. Inaugural Session <br />
          2. Mechanical / CSE / Electrical
        </p>
        <p>
          TB-10 <br />
          1. BBA/MBA
        </p>
        <p>
          FB-05 <br />
          1. BSc/MSc/Others
        </p>
        <p>
          FB-08 (Robotics lab)<br />
          1. Civil / Metallurgy / Other Engineering Branches
        </p>
      </div>

      <!-- event Content Of Presentation -->
      <div class="detail-rules">
        <h2>{{ 'Content Of Presentation'.toUpperCase() }}</h2>
        <ul>
          <li>
            Title of proposed solution (in 20 words): A heading that best
            describes your solution.
          </li>
          <li>
            Problem Statement:- Describe the problem which your idea is going to
            solve.
          </li>
          <li>
            The proposed solution of the problems:- Propose a solution and
            explain how your innovative idea is going to solve that problem.
          </li>
          <li>Conclusion:- Conclusion of your idea.</li>
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
  name: 'IdeathonEventPage',
  data() {
    return {
      event: {
        name: 'Ideathon',
        img: 'ideathon.jpg',
        event_desc:
          'An Ideathon is a short, engaging brainstorming event where individuals from different backgrounds address some of the most pressing challenges of our time. Individuals and students having different skills and interests converge to diagnose predefined problems, identify the best opportunities and ideate the most viable solution.',
        teams: [
          {
            img: 'arindam.png',
            name: 'Arindam Chakraborty',
            call: '9981257969',
          },
          {
            img: 'nehapatel.png',
            name: 'Neha Patel',
            call: '9131286269',
          },
          {
            img: 'ravinderkumar.png',
            name: 'Ravinder Kumar',
            call: '8770670706',
          },
          {
            img: 'vishalpandey.png',
            name: 'Vishal Pandey',
            call: '6207005596',
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

      table {
        tbody {
          tr {
            td {
              // margin: 0 1rem;
              padding: 0.5rem 0.5rem 0.5rem 0;
              font-size: 1rem;
              word-break: break-all;
              font-family: 'Roboto', sans-serif;
              line-height: 1.4rem;
            }
          }
        }
      }

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
