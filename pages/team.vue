<template>
  <div class="team-wrapper">
    <nav-bar />
    <nav-bar-two />
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
              name: 'Dr R.D Patidar',
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
              name: 'Dr Mahesh Bhiwapurkar',
              image: 'mahesh.png',
              designation: '',
            },
            {
              name: 'Dr Sanjay Singh',
              image: 'sanjay.png',
              designation: '',
            },
          ],
        },
        {
          name: 'Faculty Conveners',
          team: [
            {
              name: 'Dr Swati Verma',
              image: 'swati.png',
              designation: '',
            },
            {
              name: 'Dr Trinath Talapaneni',
              image: 'trinath.png',
              designation: '',
            },
            {
              name: 'Dr L R Bhandarkar',
              image: 'LR.png',
              designation: '',
            },
            {
              name: 'Dr Vikash Kumar',
              image: 'vikas.png',
              designation: '',
            },
          ],
        },
        {
          name: 'Faculty Co-Conveners',
          team: [
            {
              name: 'Dr Imran Ahmad Qadri',
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
              name: 'Dr Nidhi Kobragade',
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
              name: 'Dr Deepak Patel',
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
        {
          name: 'Design and Development',
          team: [
            {
              name: 'Subrat Kumar Jena',
              image: 'subrat.png',
              designation: 'Team Lead & Developer',
            },
            {
              name: 'Surbhi Vandana',
              image: 'surbhivandana.png',
              designation: 'Designer',
            },
          ],
        },
        {
          name: 'Student Co-Convenor',
          team: [
            {
              name: 'Manish Gupta',
              image: 'manishgupta.png',
              designation: 'CSE',
            },
            {
              name: 'Tanuja Nair',
              image: 'tanuja.png',
              designation: 'CSE',
            },
            {
              name: 'Anand Raj Dansena',
              image: 'anandraj.png',
              designation: 'MECHANICAL',
            },
            {
              name: 'Shubham Yadav',
              image: 'shubhamyadav.png',
              designation: 'MECHANICAL',
            },
            {
              name: 'Sarang Suhas Bakre',
              image: 'sarang.png',
              designation: 'METALLURGY',
            },
            {
              name: 'Anusuya P',
              image: 'anusuya.png',
              designation: 'METALLURGY',
            },
            {
              name: 'Simran Patel',
              image: 'simranpatel.png',
              designation: 'CIVIL',
            },
            {
              name: 'Priyesh Prasad',
              image: 'priyeshprasad.png',
              designation: 'CIVIL',
            },
            {
              name: 'Raunak Agarwal',
              image: 'raunak.png',
              designation: 'ELECTRICAL',
            },
            {
              name: 'Bindu Sao',
              image: 'bindusao.png',
              designation: 'ELECTRICAL',
            },
            {
              name: 'Suryaranjan',
              image: 'suryaranjan.png',
              designation: 'MBA',
            },
            {
              name: 'Kusum Pandey',
              image: 'kusum.png',
              designation: 'BSc. Hons',
            },
            {
              name: 'Yashvi Solanki',
              image: 'yashvi.png',
              designation: 'B.Com',
            },
            {
              name: 'Sourabh Mehani',
              image: 'sourabh.png',
              designation: 'B.Com',
            },
            {
              name: 'Sanskar gupta',
              image: 'sanskargupta.png',
              designation: 'BBA',
            },
            {
              name: 'Tejeswar verma',
              image: 'tejeswarverma.png',
              designation: 'BBA',
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
    padding: 8rem 0;
    .heading {
      font-size: 3rem;
      color: #fff;
      margin: 1rem auto;
      width: fit-content;
      font-family: 'Montserrat', sans-serif;
      font-weight: bolder;
    }

    .card {
      padding: 0 1.5rem;
      margin: 3rem 1.2rem;

      .card-title {
        text-align: center;
        color: #fff;
        font-size: 2rem;
        font-family: 'Montserrat', sans-serif;
        font-weight: 700;
      }

      .members {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-wrap: wrap;
      }
    }
  }
}

@media all and (max-width: '1248px') {
  .team-wrapper {
    .team-card-container {
      padding: 2rem 0;
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
        .members {
          justify-content: center;
        }
      }
    }
  }
}
</style>
