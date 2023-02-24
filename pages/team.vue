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
            data-aos="fade-up"
            data-aos-delay="100"
          />
        </div>
      </div>
    </div>
    <nav-bar-three />
  </div>
</template>

<script>
export default {
  name: 'TeamPage',
  data() {
    return {
      teams: [
        // {
        //   name: 'Patron',
        //   team: [
        //     {
        //       name: 'Ms. Shallu Jindal',
        //       image: 'shallu.png',
        //       designation: 'Chancellor, OPJU',
        //     },
        //   ],
        // },
        // {
        //   name: 'Leadership Team',
        //   team: [
        //     {
        //       name: 'Dr R.D Patidar',
        //       image: 'RD.png',
        //       designation: 'Vice Chancellor, OPJU',
        //     },
        //     {
        //       name: 'Mr. Anurag Vijaywargya',
        //       image: 'vijay.png',
        //       designation: 'Registrar, OPJU',
        //     },
        //   ],
        // },

        // student conveners
        {
          name: 'Student Convenors',
          team: [
            {
              name: 'Chirag Mishra',
              image: 'chiragmishra.jpg',
              designation: 'MECHANICAL',
              call: '+918871724185',
              mail: 'chiragmishra0501@gmail.com',
            },
            {
              name: 'ADITYA SHEKHAR',
              image: 'adityashekhar.jpeg',
              designation: 'MECHANICAL',
              call: '+918529768326',
              mail: 'Adityashekhar57@gmail.com ',
            },
            {
              name: 'RITISHA AGRAWAL',
              image: '',
              designation: 'EE',
              call: '+917587230147',
            },
            {
              name: 'SHIVAM PANDEY',
              image: 'shivampandey.png',
              designation: 'EE',
              call: '+917000662948',
            },
            {
              name: 'ABHINAV SHARMA',
              image: '',
              designation: 'CIVIL',
              call: '+917477028878',
            },
            {
              name: 'ANAND PATEL',
              image: 'anandpatel.png',
              designation: 'CIVIL',
              call: '+916266819393',
            },
            {
              name: 'SUSHANT MISHRA',
              image: '',
              designation: 'CSE',
              call: '+917067718336',
            },
            {
              name: 'SIMRELLA AGRAWAL',
              image: 'simrellaagrawal.png',
              designation: 'CSE',
              call: '+917489211170',
              mail: 'simsim44144@gmail.com',
            },
            {
              name: 'DEENDAYAL PRAJAPATI',
              image: '',
              designation: 'META',
              call: '+917489559277',
            },
            {
              name: 'ARJUN GUPTA',
              image: '',
              designation: 'META',
              call: '+919630526890',
            },
            {
              name: 'SHUBHAM KUAMR ADDI',
              image: '',
              designation: 'META',
              call: '+919142716619',
            },
            {
              name: 'AKHILESH',
              image: '',
              designation: 'META',
              call: '+918789916216',
            },
            {
              name: 'RITIKA SAINI',
              image: 'ritikasaini.png',
              designation: 'SOS',
              call: '+916264824855',
            },
            {
              name: 'TANKESHWER PATEL',
              image: '',
              designation: 'SOS',
              call: '+917803064829',
            },
            {
              name: 'ASTHA GUPTA',
              image: 'asthgupta.jpeg',
              designation: 'SOS',
              call: '+916267138484',
              mail: 'asth.ug20bscch01@opju.ac.in',
            },
            {
              name: 'SHIVAM SHAW',
              image: 'shivamshaw.jpg',
              designation: 'SOM (MBA)',
              call: '+917278294467',
              mail: 'shivamshaw034@gmail.com',
            },
            {
              name: 'AASHISH KUMAR GUPTA',
              image: '',
              designation: 'SOM (BBA)',
              call: '+919907499711',
            },
            {
              name: 'VIPUL KUMAR',
              image: 'vipulkumar.jpg',
              designation: 'SOM (MBA)',
              call: '+917224898002',
              mail: 'vipu.mba2163@opju.ac.in',
            },
            {
              name: 'MUSHKAN BERIWAL',
              image: '',
              designation: 'SOM (BCOM)',
              call: '+917745924214',
            },
            {
              name: 'AYUSH PANDEY',
              image: 'ayushpandey.jpg',
              call: '+917974670576',
              mail: 'Ayushpandey1310@gmail.com',
            },
            {
              name: 'KALYANI',
              image: 'kalyani.jpg',
              call: '+918305216654',
              mail: 'Sankhasingh777@gmail.com',
            },
            {
              name: 'Tankeshwar Patel',
              image: 'tankeshwar.jpg',
            },
          ],
        },

        // student co-conveners
        {
          name: 'Student Co-Convenors',
          team: [
            {
              name: 'Manish Gupta',
              image: 'manishgupta.png',
              designation: 'CSE',
              call: '+919131391650',
              mail: 'mani.ug20cse24@opju.ac.in',
            },
            {
              name: 'Tanuja Nair',
              image: 'tanuja.png',
              designation: 'CSE',
              call: '+916263374001',
              mail: 'tanu.ug20cse52@opju.ac.in',
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
              name: 'Rounak Agarwal',
              image: 'raunak.png',
              designation: 'ELECTRICAL',
              call: '+919304043774',
              mail: 'roun.ug20ee13@opju.ac.in',
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

        // faculty convenors
        {
          name: 'Faculty Convenors',
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
              designation: '( junoon )',
            },
          ],
        },

        // faculty co-convenors
        {
          name: 'Faculty Co-Convenors',
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

        // faculty mentors
        // {
        //   name: 'Faculty Mentors',
        //   team: [
        //     {
        //       name: 'Dr Mahesh Bhiwapurkar',
        //       image: 'mahesh.png',
        //       designation: '',
        //     },
        //     {
        //       name: 'Dr Sanjay Singh',
        //       image: 'sanjay.png',
        //       designation: '',
        //     },
        //   ],
        // },

        // {
        //   name: 'Faculty Coordinators',
        //   team: [
        //     {
        //       name: 'Prof. Sikha Tiwari',
        //       image: 'sikha.png',
        //       designation: '',
        //     },
        //     {
        //       name: 'Prof. Pradeep Shrivas',
        //       image: 'pradeep.png',
        //       designation: '',
        //     },
        //     {
        //       name: 'Dr Nidhi Khobragade',
        //       image: 'nidhi.png',
        //       designation: '',
        //     },
        //     {
        //       name: 'Prof. Dharmender Singh Saini',
        //       image: 'dharmender.png',
        //       designation: '',
        //     },
        //     {
        //       name: 'Prof. Ankireddy Narendra',
        //       image: 'ankireddy.png',
        //       designation: '',
        //     },
        //     {
        //       name: 'Dr Deepak Patel',
        //       image: 'deepak.png',
        //       designation: '',
        //     },
        //     {
        //       name: 'Prof. Manoj Kumar Mishra',
        //       image: 'manoj.png',
        //       designation: '',
        //     },
        //   ],
        // },

        // design and dev
        {
          name: 'Design and Development',
          team: [
            {
              name: 'Subrat Kumar Jena',
              image: 'subrat.png',
              designation: 'Developer',
            },
            {
              name: 'Surbhi Vandana',
              image: 'surbhivandana.png',
              designation: 'Designer',
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
        font-size: 2.1rem;
        text-align: center;
      }
      .card {
        padding: 0;
        .card-title {
          text-align: center;
          font-size: 1.8rem;
        }
        .members {
          justify-content: center;
        }
      }
    }
  }
}
</style>
