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
              image: 'shallu.png',
              designation: 'Chancellor, OPJU',
            },
          ],
        },
        {
          name: 'Leadership Team',
          team: [
            {
              name: 'Dr. R.D Patidar',
              image: 'RD.png',
              designation: 'Vice Chancellor, OPJU',
            },
            {
              name: 'Mr. Anurag Vijaywargya',
              image: 'vijay.png',
              designation: 'Registrar, OPJU',
            },
          ],
        },
        {
          name: 'Faculty Mentors',
          team: [
            {
              name: 'Dr. Mahesh Bhiwapurkar',
              image: 'mahesh.png',
              designation: '',
            },
          ],
        },
        {
          name: 'Faculty Conveners',
          team: [
            {
              name: 'Dr. Swati Verma',
              image: 'swati.png',
              designation: '',
            },
            {
              name: 'Dr. Trinath Talapaneni',
              image: 'trinath.png',
              designation: '',
            },
            {
              name: 'Prof. L R Bhandarkar',
              image: 'LR.png',
              designation: '',
            },
            {
              name: 'Dr. Vikash Kumar',
              image: 'vikas.png',
              designation: '',
            },
          ],
        },
        {
          name: 'Faculty Co-conveners',
          team: [
            {
              name: 'Dr. Imran Ahmad Qadri',
              image: 'imran.png',
              designation: '',
            },
            {
              name: 'Prof. Princy Diwan',
              image: 'princy.png',
              designation: '',
            },
            {
              name: 'Prof. Sujata Panda',
              image: 'sujata.png',
              designation: '',
            },
            {
              name: 'Prof. Pushpanjali Shadangi',
              image: 'pushpanjali.png',
              designation: '',
            },
          ],
        },
        {
          name: 'Faculty Coordinators',
          team: [
            {
              name: 'Prof. Sikha Tiwari',
              image: 'sikha.png',
              designation: '',
            },
            {
              name: 'Prof. Pradeep Shrivas',
              image: 'pradeep.png',
              designation: '',
            },
            {
              name: 'Dr. Nidhi Kobragade',
              image: 'nidhi.png',
              designation: '',
            },
            {
              name: 'Prof. Dharmender Singh Saini',
              image: 'dharmender.png',
              designation: '',
            },
            {
              name: 'Prof. Ankireddy Narendra',
              image: 'ankireddy.png',
              designation: '',
            },
            {
              name: 'Dr. Deepak Patel',
              image: 'deepak.png',
              designation: '',
            },
            {
              name: 'Prof. Manoj Kumar Mishra',
              image: 'manoj.png',
              designation: '',
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
  background-image: linear-gradient(to bottom, #6308492d, #0e0e5552);
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
      padding: 0 1.5rem;
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
      .card {
        padding: 0;
        .card-title {
          text-align: center;
        }
      }
    }
  }
}
</style>
