<template>
  <div>
    <nav-bar />
    <nav-bar-two />
    <nav-bar-three />
    <div class="sponsors-container">
      <p class="page-title">sponsors</p>
      <div class="sponsors-lists">
        <div
          v-for="(sponsor, i) in sponsors"
          :key="i"
          class="sponsors-card"
          data-aos="fade-up"
          data-aos-delay="100"
        >
          <nuxt-img
            :src="'/sponsors/' + sponsor.img"
            format="webp"
            loading="lazy"
          />
          <span class="sponsor-title">sponsors of {{ sponsor.name }}</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SponsorsPage',
  data() {
    return {
      sponsors: [
        {
          img: 'Prism medical.png',
          name: 'Antaragni',
        },
        {
          img: 'sunil medical .png',
          name: 'Antaragni',
        },
      ],
    }
  },
}
</script>

<style lang="scss" scoped>
.sponsors-container {
  background: #000;
  background-image: linear-gradient(to bottom, #41195f2d, #000000);
  min-height: 100vh;
  max-height: 100%;
  width: 100vw;
  padding: 8rem 3rem 2rem 3rem;
  color: #fff;

  .page-title {
    font-family: 'Poppins', sans-serif;
    font-weight: bold;
    font-size: 3rem;
    letter-spacing: 0.02em;
    width: 100%;
    background: -webkit-linear-gradient(#d6d6d6, #e3e3e3e5);
    background-clip: text;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    text-shadow: rgba(255, 255, 255, 0.466) 0px 0px 5px,
      rgba(243, 243, 243, 0.836) 0px 0px 30px;
    text-transform: uppercase;
    text-align: center;
  }

  .sponsors-lists {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-evenly;
    margin-top: 5rem;

    .sponsors-card {
      background-color: #e6e6e6;
      border-radius: 4px;
      display: flex;
      flex-direction: column;
      //   justify-content: center;
      align-items: center;
      position: relative;
      margin: 1rem 0;

      img {
        height: 300px;
        width: 100%;
      }

      .sponsor-title {
        color: #000000;
        position: absolute;
        bottom: 10%;
        font-size: 1.1rem;
        font-family: 'Montserrat', sans-serif;
        font-weight: 600;
        text-transform: uppercase;
        letter-spacing: 0.01em;
      }
    }
  }
}

@media all and (max-width: '1248px') {
  .sponsors-container {
    padding: 4rem 2rem 2rem 2rem;
  }
}

@media all and (max-width: '912px') {
  .sponsors-container {
    .page-title {
      font-size: 2.5rem;
    }

    .sponsors-lists {
      margin-top: 1rem;
    }

    .event-lists {
      margin-top: 3rem;
    }
  }
}
</style>
