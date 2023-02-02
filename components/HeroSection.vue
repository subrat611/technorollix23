<template>
  <div class="hero-wrapper">
    <div class="bg-video">
      <!-- <video
        autoplay
        loop
        muted
        src="~/assets/videos/hero-bg-video1.mp4"
      ></video> -->
      <nuxt-img src="hero-bg.png" format="webp" />
    </div>
    <div class="content">
      <div class="prize-pool-mob-wrapper">
        <nuxt-img src="/prize-pool.png" height="110" />
        <div class="prize-pool-mob-text">
          <span>prize pool</span>
          <span><b>₹</b> 3,00,000</span>
        </div>
      </div>
      <p class="techno-sub top--title">
        A National Level<br />
        Techno-Cultural Fest
      </p>
      <div class="techno-title">
        <div class="prize-pool-wrapper">
          <div class="prize-pool-board">
            <p class="prize-pool-text--top">prize pool</p>
            <span class="prize-pool-text--bottom">₹3,00,000</span>
          </div>
          <nuxt-img src="/person-holding-board.png" class="prize-pool-person" />
        </div>
        TECHNOROLLIX
      </div>
      <p class="techno-sub">2023</p>
      <p class="techno-date">
        MARCH 1<sup style="font-family: 'origin Tech'; font-size: 0.9rem"
          >st</sup
        >
        - 4<sup style="font-family: 'origin Tech'; font-size: 0.9rem">th</sup>
      </p>
      <!-- <p class="reg-btn" @click="$router.push('register')">Register</p> -->
    </div>
  </div>
</template>

<script>
export default {
  name: 'HeroSection',
  head: {
    title: "Technorollix'23 | O.P Jindal University",
  },
}
</script>

<style lang="scss" scoped>
.hero-wrapper {
  height: 100vh;
  width: 100vw;
  position: relative;

  .bg-video {
    height: 100%;
    width: 100vw;
    position: relative;

    video {
      position: absolute;
      top: 0;
      left: 0;
      height: 100%;
      width: 100%;
      object-fit: cover;
    }
    img {
      position: absolute;
      top: 0;
      left: 0;
      height: 100%;
      width: 100%;
      object-fit: cover;
      filter: blur(1px);
    }
  }

  .content {
    position: absolute;
    top: 0;
    left: 0;
    height: 100%;
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding-top: 0;

    .prize-pool-mob-wrapper {
      display: none;
      align-items: center;
      position: relative;

      .prize-pool-mob-text {
        position: absolute;
        top: 60%;
        right: -25%;
        transform: translate(0, -50%);
        display: flex;
        flex-direction: column;
        text-align: center;

        span {
          font-family: 'origin Tech';
          font-size: 1.2rem;
          color: #fff;
          text-shadow: rgba(91, 213, 247, 0.493) 0px 0px 15px,
            rgba(91, 212, 247, 1) 0px 0px 15px,
            rgba(91, 213, 247, 0.61) 0px 0px 15px;
        }
      }
    }

    .techno-title {
      font-size: 7rem;
      color: #fff;
      font-weight: 800;
      // font-family: 'Montserrat', sans-serif;
      font-family: 'origin Tech';
      letter-spacing: 0.1em;
      text-shadow: rgb(255, 120, 239, 0.5) 0px 0px 15px,
        rgb(255, 120, 239, 0.5) 0px 0px 15px, rgb(255, 120, 239, 1) 0px 0px 15px;
      position: relative;

      .prize-pool-wrapper {
        position: absolute;
        top: 0;
        height: 100%;
        width: 100%;

        .prize-pool-board {
          position: absolute;
          right: -10%;
          top: -179%;
          background: rgba(63, 194, 255, 0.11);
          border: 1px solid #fff;
          border-radius: 7px;
          box-shadow: 0 4px 30px rgb(104 104 104 / 10%);
          box-shadow: rgba(10, 50, 61, 0.521) 0px 0px 15px,
            rgba(91, 213, 247, 0.555) 0px 0px 15px,
            rgba(91, 213, 247, 0.5) 0px 0px 15px;
          backdrop-filter: blur(3.3px);
          z-index: 1;

          .prize-pool-text--top,
          .prize-pool-text--bottom {
            display: block;
            font-family: 'origin Tech';
            font-size: 2rem;
            letter-spacing: 0.11em;
            padding: 1rem;
            text-align: center;

            text-shadow: rgba(132, 220, 207, 0.7) 0px 0px 10px,
              rgba(7, 63, 55, 0.815) 0px 0px 10px;
          }
        }

        .prize-pool-person {
          position: absolute;
          right: -10%;
          bottom: 0;
          height: 160px;
        }
      }
    }

    .techno-sub.top--title {
      text-align: center;
      font-size: 2rem;
      padding-bottom: 1rem;
      text-shadow: rgba(10, 50, 61, 0.521) 0px 0px 15px,
        rgba(91, 213, 247, 0.616) 0px 0px 15px,
        rgba(91, 212, 247, 1) 0px 0px 15px;
    }

    .techno-sub {
      margin-top: 1rem;
      text-align: center;
      color: #fff;
      font-size: 5.6rem;
      font-family: 'origin Tech';
      text-shadow: rgba(91, 213, 247, 0.493) 0px 0px 15px,
        rgba(91, 212, 247, 1) 0px 0px 15px,
        rgba(91, 213, 247, 0.61) 0px 0px 15px;
    }

    .techno-date {
      margin-top: 0.5em;
      font-size: 2rem;
      color: #fff;
      font-family: 'origin Tech';
      // text-shadow: rgba(91, 212, 247, 0.5) 0px 0px 10px,
      //   rgba(91, 212, 247, 0.8) 0px 0px 12px, rgba(91, 212, 247, 1) 0px 0px 10px;
      text-shadow: rgba(132, 220, 207, 0.7) 0px 0px 10px,
        rgba(7, 63, 55, 0.815) 0px 0px 10px;
    }

    .reg-btn {
      margin-top: 0.9rem;
      padding: 0.6em 1.7rem;
      background: rgba(63, 194, 255, 0.11);
      border-radius: 3px;
      box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
      backdrop-filter: blur(3.3px);
      -webkit-backdrop-filter: blur(3.3px);
      border: 1px solid rgba(63, 194, 255, 0.63);
      font-weight: normal;
      font-size: 1.3rem;
      color: #fff;
      text-shadow: rgba(63, 194, 255, 0.63) 0px 0px 6px,
        rgba(63, 194, 255, 0.63) 0px 0px 5px;
      cursor: pointer;

      &:hover {
        background: rgba(63, 194, 255, 0.19);
      }
    }
  }
}

@media all and (max-width: '1231px') {
  .hero-wrapper {
    .content {
      .prize-pool-mob-wrapper {
        display: flex;
        align-items: center;
        position: relative;
      }
      .techno-title {
        .prize-pool-wrapper {
          display: none;
        }
      }
    }
  }
}

@media all and (max-width: '912px') {
  .hero-wrapper {
    .content {
      .techno-title {
        font-size: 2.3rem;
      }
      .techno-sub.top--title {
        font-size: 1.2rem;
      }
      .techno-sub {
        font-size: 1.3rem;
      }
      .techno-date {
        font-size: 1.1rem;
      }
      .reg-btn {
        font-size: 1.05rem;
      }
    }
  }
}
</style>
