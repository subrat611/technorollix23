<template>
  <div class="team-wrapper">
    <nav-bar />
    <div class="team-card-container">
      <p class="heading">Technorollix'23 Team</p>
      <div v-for="team in teams" :key="team.name" class="card">
        <p class="card-title">{{ team.name }}</p>
        <div class="members">
          <team-card
            v-for="(member, i) in team.team"
            :key="i"
            :member="member"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TeamPage',
  data() {
    return {
      teams: [
        {
          name: 'Patron',
          team: [
            {
              name: 'Ms. Shallu Jindal',
              image: '1.JPG',
              designation: 'Chancellor, OPJU',
            },
            {
              name: 'Ms. Shallu Jindal',
              image: '1.JPG',
              designation: 'Chancellor, OPJU',
            },
          ],
        },
        {
          name: 'Mentors',
          team: [
            {
              name: 'Ms. Shallu Jindal',
              image: '1.JPG',
              designation: 'Chancellor, OPJU',
            },
            {
              name: 'Ms. Shallu Jindal',
              image: '1.JPG',
              designation: 'Chancellor, OPJU',
            },
          ],
        },
        {
          name: 'Conveners',
          team: [
            {
              name: 'Ms. Shallu Jindal',
              image: '1.JPG',
              designation: 'Chancellor, OPJU',
            },
            {
              name: 'Ms. Shallu Jindal',
              image: '1.JPG',
              designation: 'Chancellor, OPJU',
            },
          ],
        },
        {
          name: 'Co-conveners',
          team: [
            {
              name: 'Ms. Shallu Jindal',
              image: '1.JPG',
              designation: 'Chancellor, OPJU',
            },
            {
              name: 'Ms. Shallu Jindal',
              image: '1.JPG',
              designation: 'Chancellor, OPJU',
            },
          ],
        },
        {
          name: 'Coordinators',
          team: [
            {
              name: 'Ms. Shallu Jindal',
              image: '1.JPG',
              designation: 'Chancellor, OPJU',
            },
            {
              name: 'Ms. Shallu Jindal',
              image: '1.JPG',
              designation: 'Chancellor, OPJU',
            },
          ],
        },
      ],
    }
  },
}
</script>

<style lang="scss" scoped>
.team-wrapper {
  background: #000;
  // background-image: linear-gradient(to bottom, #30022456, #19191a52);
  background-repeat: no-repeat;
  min-height: 100vh;
  max-height: 100%;

  .team-card-container {
    .heading {
      font-size: 3rem;
      color: #fff;
      margin: 1rem auto;
      width: fit-content;
      font-family: 'Montserrat', sans-serif;
      font-weight: bolder;
    }

    padding: 2rem 0;
    .card {
      margin: 5rem 1.2rem;

      .card-title {
        color: #fff;
        font-size: 2rem;
        font-family: 'Montserrat', sans-serif;
        font-weight: 700;
      }

      .members {
        display: flex;
        flex-wrap: wrap;
      }
    }
  }
}

@media all and (max-width: '912px') {
  .team-wrapper {
    .team-card-container {
      .heading {
        font-size: 1.5rem;
      }
    }
  }
}
</style>
