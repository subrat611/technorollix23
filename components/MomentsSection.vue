<template>
  <div class="pride-moments">
    <div class="pride-moment-bg">
      <img src="~/assets/img/bg.png" alt="background" />
      <div class="overlay"></div>
    </div>
    <div class="content">
      <div class="main-text">
        <span class="title">Our Pride Moments</span>
      </div>
      <div class="images-on-scroll">
        <div class="container">
          <div class="image-container">
            <img
              class="pride-img"
              src="~/assets/img/moments/1-min.JPG"
              alt="pride-moments-pic"
              draggable="false"
            />
            <img
              class="pride-img"
              src="~/assets/img/moments/2-min.JPG"
              alt="pride-moments-pic"
              draggable="false"
            />
          </div>
          <div class="image-container">
            <img
              src="~/assets/img/moments/4-min.JPG"
              alt="pride-moments-pic"
              draggable="false"
            />
            <img
              src="~/assets/img/moments/5-min.JPG"
              alt="pride-moments-pic"
              draggable="false"
            />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { gsap } from 'gsap'

export default {
  name: 'MomentsSection',
  mounted() {
    gsap.registerPlugin('ScrollTrigger')

    gsap.to('.image-container', {
      yPercent: -100,
      duration: 12,
      repeat: -1,
      yoyo: true,
    })
  },
}
</script>

<style lang="scss" scoped>
.pride-moments {
  height: 100vh;
  width: 100vw;
  position: relative;

  .pride-moment-bg {
    height: 100%;
    position: relative;

    img {
      filter: blur(1.3px);
      position: absolute;
      top: 0;
      left: 0;
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
      background-image: linear-gradient(
        109.6deg,
        rgba(209, 0, 116, 1) 11.2%,
        rgba(110, 44, 107, 1) 91.1%
      );
      opacity: 0.2;
    }
  }

  .content {
    position: absolute;
    height: 100%;
    width: 100%;
    top: 0;
    left: 0;

    .main-text {
      height: 100%;
      width: 100%;
      display: flex;
      justify-content: center;
      align-items: center;

      .title {
        color: #fff;
        font-size: 6.2rem;
        font-family: 'Montserrat', sans-serif;
        font-weight: 700;
      }
    }

    .images-on-scroll {
      position: absolute;
      top: 0;
      left: 0;
      height: 100%;
      width: 100%;

      .container {
        position: relative;
        height: 100%;
        overflow: hidden;

        .image-container {
          position: relative;
          height: 100%;

          img {
            position: absolute;
            top: 0;
            left: 0;
            height: 40%;
            width: 30%;
            border-radius: 4px;
            box-shadow: rgba(0, 0, 0, 0.05) 0px 6px 24px 0px,
              rgba(0, 0, 0, 0.08) 0px 0px 0px 1px;
          }

          img:nth-child(1) {
            top: 20%;
            left: 10%;
            transform: rotate(-5deg);
          }

          img:nth-child(2) {
            top: 40%;
            left: 60%;
            transform: rotate(-5deg);
          }
        }
      }
    }
  }
}

@media all and (max-width: '912px') {
  .pride-moments {
    .content {
      .main-text {
        .title {
          font-size: 2rem;
        }
      }
      .images-on-scroll {
        .container {
          width: 100%;
          .image-container {
            height: 80%;
            width: 100%;
            display: flex;
            flex-direction: column;
            align-items: center;
            img {
              position: relative;
              height: 200px;
              width: 300px;
            }
            img:nth-child(1) {
              left: -3%;
              transform: rotate(0);
            }
            img:nth-child(2) {
              left: 5%;
              transform: rotate(0);
            }
          }
        }
      }
    }
  }
}
</style>
