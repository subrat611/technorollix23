<template>
  <div class="about-page">
    <nav-bar />

    <!-- about container -->
    <div class="about-container">
      <!-- image container -->
      <div class="image-container">
        <nuxt-img
          src="/opju-image.png"
          format="webp"
          loading="lazy"
          class="opju-bg-image"
        />
        <div class="overlay"></div>
        <p class="title">about us</p>
      </div>

      <!-- about -->
      <div class="about-content">
        <!-- about opju -->
        <div class="about-opju">
          <p class="about-title">about o.p. jindal university</p>
          <p class="about-para">
            Founded by the Jindal Educaticdon and Welfare Society, OP Jindal
            University (OPJU) was set up to bring high quality education to its
            students based on a world class curriculum, the latest teaching
            methodology and committed faculty members. The multidisciplinary
            university aims to develop young professionals and future leaders
            who will not only power growth and development in the state, but
            also make a mark globally.At the core of the university's philosophy
            and approach lies the belief that students learn best when exposed
            to real world situations and when nurtured through enriching
            interactions with practitioners and professors. We at OPJU believe
            that every student has innate potential that can be unlocked through
            quality teaching and mentorship.
          </p>
        </div>

        <!-- patron message -->
        <div class="patron-container">
          <p class="patron-title-one">patron's message</p>
          <p class="patron-title-two">
            SHRI NAVEEN JINDAL Chairman, Jindal Steel and Power Ltd
          </p>
          <p class="patron-para-one">
            When OPJU was established 8 years ago in Punjipathra, Raigarh
            District it was the culmination of the dream of my father and the
            founding Chairman of OP Jindal Group, Shri O. P. Jindal. JSPL’s
            humble beginnings are rooted in the District of Raigarh, where it
            began as a small steel making operation in the early 1990’s and
            through the hard work and dedication of the founders and employees
            today boasts of a 3.6 MTPA steel plant, a 3400 MW Power plant in
            Tamnar – the first independent power producer, Nalwa Steel Works,
            Structural Steel Division, and OP Jindal Industrial Park,
            Punjipathra. For a community that means so much to the success of
            JSPL, it was our dream to start a University in the area as both a
            way to give back to the region, but more so, a deeply rooted
            commitment to educate the youth of the area, as only an educated
            youth can help the nation develop to its full potential.
          </p>
          <p class="patron-para-two">
            Started in 2008 as an engineering college, today I can proudly say
            that in a short span of only four years, OPJU has become a role
            model for institutions of higher education not only in Chhattisgarh,
            but in the entire nation of what can be achieved with the right
            motivations, vision, and programs focused on student outcomes,
            creating vast employment opportunities for the youth of our nation
            and guiding them along a path to becoming successful contributors to
            society. With OP Jindal Group’s deep commitment to nation building
            and focus on core industries of Steel, Mining, Power, and
            Construction, it is only befitting that OPJU’s vision of becoming
            the nation’s first private and only university to enhance the core
            sector capabilities is our commitment to the growth of the nation
            and realizing our collective dream of building the nation we can all
            be proud of. As the Patron of an institution of higher learning, I
            am humbled by the enormous faith the community has bestowed upon me
            and accept the challenge and the responsibility to build a socially
            responsible, equitable, and accessible institute we can all take
            pride in.
          </p>
        </div>

        <!-- about technorollix -->
        <div class="about-techno">
          <p class="techno-title">about technorollix</p>
          <p class="techno-para">
            Welcome to Central India's Biggest Technial And Cultural Fest
            <span class="techno">#Technorollix.</span>This event is organized
            yearly by our students and faculty staff. This event is called the
            Biggest Technical and Cultural because of its variety in every
            possible way possible. This fest includes each and every competition
            and event you can think off from art to gaming, from talks to
            exhibitions, each and every event has its own charm. Technorollix,
            the annual techno-Management festival of OP Jindal University, hosts
            a galaxy of events aimed at boosting the technological and cultural
            skills inherent in today’s youth, giving them an unrivalled
            opportunity to showcase their thoughts and ideas. Over the last four
            years, it has been a platform that has successfully brought
            students, academicians, and industrial giants under one roof.
            Technorollix’23, Spanning from 1<sup>th</sup> March 2023 to 4<sup
              >th</sup
            >
            March 2023, aims at giving a spine-tingling ride to inspiring minds
            and bringing together dynamic, innovative and enterprising students
            of various colleges (students of B Tech., B.Com, B.Sc., BBA) from
            all over India on a common platform to participate in different
            competitive events along with OPJU students, dedicated to
            experiencing the fun in technology, Management and science.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AboutUs',
}
</script>

<style lang="scss" scoped>
.about-page {
  background: #000;

  .about-container {
    color: #fff;
    .image-container {
      position: relative;
      height: 350px;
      width: 100vw;

      .opju-bg-image {
        position: absolute;
        height: 100%;
        width: 100%;
        object-fit: cover;
      }

      .overlay {
        position: absolute;
        top: 0;
        left: 0;
        height: 100%;
        width: 100%;
        background-color: #000;
        opacity: 0.6;
      }

      .title {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        font-size: 4rem;
        font-family: 'Montserrat', sans-serif;
        letter-spacing: 0.15em;
        text-transform: uppercase;
        color: #e9ecef;
        font-weight: bold;
      }
    }

    .about-content {
      margin-top: 1rem;
      padding: 2rem 5rem;
      font-family: 'Poppins', sans-serif;

      .about-opju {
        margin-bottom: 2rem;
        .about-title {
          font-size: 2rem;
          text-transform: capitalize;
          margin-bottom: 1.5rem;
          font-weight: 600;
        }

        .about-para {
          font-family: 'Montserrat', sans-serif;
          color: #dee2e6;
          text-align: justify;
          line-height: 1.5rem;
          font-size: 1.15rem;
        }
      }

      .patron-container {
        margin-bottom: 2rem;

        .patron-title-one {
          font-size: 2rem;
          text-transform: capitalize;
          margin-bottom: 1rem;
          font-weight: 600;
        }

        .patron-title-two {
          font-size: 1.5rem;
          padding: 0.5rem 0;
        }

        .patron-para-one {
          color: #dee2e6;
          font-family: 'Montserrat', sans-serif;
          text-align: justify;
          line-height: 1.5rem;
          font-size: 1.15rem;
        }

        .patron-para-two {
          font-family: 'Montserrat', sans-serif;
          margin-top: 1.2rem;
          color: #dee2e6;
          text-align: justify;
          line-height: 1.5rem;
          font-size: 1.15rem;
        }
      }

      .about-techno {
        margin-bottom: 2rem;
        .techno-title {
          font-size: 2rem;
          text-transform: capitalize;
          margin-bottom: 1rem;
          font-weight: 600;
        }
        .techno-para {
          color: #dee2e6;
          font-family: 'Montserrat', sans-serif;
          text-align: justify;
          line-height: 1.5rem;
          font-size: 1.15rem;

          .techno {
            color: orange;
          }
        }
      }
    }
  }
}

@media all and (max-width: '912px') {
  .about-page {
    .about-container {
      .image-container {
        height: 250px;

        .title {
          font-size: 1.5rem;
          text-align: center;
        }
      }

      .about-content {
        padding: 2rem;

        .about-opju {
          .about-title {
            text-align: center;
          }
          .about-para {
            min-width: 300px;
            max-width: 100%;
            text-align: left;
            line-height: 1.5rem;
            font-size: 1rem;
          }
        }

        .patron-container {
          .patron-title-one {
            text-align: center;
          }
          .patron-para-one,
          .patron-para-two {
            min-width: 300px;
            max-width: 100%;
            text-align: left;
            line-height: 1.5rem;
            font-size: 1rem;
          }
        }

        .about-techno {
          .techno-title {
            text-align: center;
          }
          .techno-para {
            min-width: 300px;
            max-width: 100%;
            text-align: left;
            line-height: 1.5rem;
            font-size: 1rem;
          }
        }
      }
    }
  }
}
</style>
