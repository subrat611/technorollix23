<template>
  <div class="main-wrapper">
    <pre-loader v-show="isLoad"></pre-loader>
    <div v-show="!isLoad" class="hero-wrapper">
      <div class="hero-img">
        <div class="darshan-img">
          <img src="~/assets/img/darshan.jpg" alt="darshan-image" />
        </div>
        <div class="jubin-img">
          <img src="~/assets/img/jubin-guitar.jpg" alt="jubin-image" />
        </div>
        <div class="shirely-img">
          <img src="~/assets/img/shirely.jpg" alt="shirely-image" />
        </div>
        <div class="bg-blur"></div>
        <div class="bg-color"></div>
      </div>
      <div class="hero-text">
        <div>
          <p>Junoon</p>
        </div>
        <div class="reg-btn">
          <span>Get ticket</span>
          <svg
            version="1.0"
            xmlns="http://www.w3.org/2000/svg"
            width="32.000000pt"
            height="32.000000pt"
            viewBox="0 0 32.000000 32.000000"
            preserveAspectRatio="xMidYMid meet"
          >
            <g
              transform="translate(0.000000,32.000000) scale(0.100000,-0.100000)"
              fill="#c916ab"
              stroke="none"
            >
              <path
                d="M260 216 c0 -5 7 -18 17 -28 16 -17 11 -18 -125 -18 -88 0 -142 -4
-142 -10 0 -6 54 -10 142 -10 141 0 141 0 123 -20 -30 -33 -11 -32 20 0 l29
30 -32 33 c-18 17 -32 28 -32 23z"
              />
            </g>
          </svg>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      isLoad: true,
    }
  },
  mounted() {
    if (!sessionStorage.getItem('allowLoader')) {
      setTimeout(() => {
        this.isLoad = false
        sessionStorage.setItem('allowLoader', false)
      }, 4100)
    } else {
      setTimeout(() => {
        this.isLoad = false
        sessionStorage.setItem('allowLoader', false)
      }, 0)
    }
  },
}
</script>

<style lang="scss" scoped>
.main-wrapper {
  height: 100%;
  width: 100vw;

  .hero-wrapper {
    width: 100%;
    height: 100vh;
    position: relative;

    .hero-img {
      height: 100%;
      display: flex;
      position: relative;

      .darshan-img,
      .jubin-img,
      .shirely-img {
        height: 100vh;

        img {
          width: 100%;
          height: 100%;
          object-fit: cover;
          object-position: center;
        }
      }

      .shirely-img {
        img {
          object-position: 15% center;
        }
      }

      .bg-color,
      .bg-blur {
        position: absolute;
        top: 0;
        left: 0;
        height: 100%;
        width: 100%;
      }

      .bg-color {
        // opacity: 0.5;
        // background-image: linear-gradient(
        //   109.6deg,
        //   rgba(45, 116, 213, 1) 11.2%,
        //   rgba(121, 137, 212, 1) 91.2%
        // );
        // background: #ff0084; /* fallback for old browsers */
        // background: -webkit-linear-gradient(
        //   to left,
        //   #33001b,
        //   #ff0084
        // ); /* Chrome 10-25, Safari 5.1-6 */
        // background: linear-gradient(
        //   to left,
        //   #33001b,
        //   #ff0084
        // ); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
        // background-image: radial-gradient(
        //   circle 610px at 5.2% 51.6%,
        //   rgba(5, 8, 114, 1) 0%,
        //   rgba(7, 3, 53, 1) 97.5%
        // );
      }

      .bg-blur {
        opacity: 0.7;
        background: #000;
        backdrop-filter: blur(6px);
      }
    }

    .hero-text {
      position: absolute;
      top: 0;
      left: 0;
      height: 100%;
      width: 100%;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      color: #fff;

      p:first-child {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        font-size: 11rem;
        // font-family: 'Gugi', cursive;
        font-family: 'adobo';
        // font-weight: 800;
        text-transform: uppercase;
        letter-spacing: 0.08em;
        color: #ffffcb;
        z-index: 2;
        // text-shadow: rgba(128, 128, 128, 0.9) 0px 0px 13px;
        text-shadow: rgba(255, 247, 94, 1) 0px 0px 24px;
        &::selection {
          background: none;
        }
      }

      // p:last-child {
      //   position: absolute;
      //   top: 60%;
      //   right: 12%;
      //   font-size: 3rem;
      //   opacity: 0.9;
      //   font-family: 'Montserrat', sans-serif;
      //   font-weight: 700;
      //   color: #e63946;
      //   letter-spacing: 0.2em;
      //   // color: #f94144;
      //   // color: #560bad;
      //   transform: translate(-50%, -50%);
      //   z-index: 1;
      // }

      .reg-btn {
        display: flex;
        align-items: center;
        margin-top: 17rem;
        cursor: pointer;

        span:first-child {
          font-family: 'Poppins', sans-serif;
          font-weight: normal;
          font-size: 1.3rem;
          color: #c916ab;
          letter-spacing: 0.02em;
          transition: all 100ms ease-in-out;
          &::selection {
            background: none;
          }
        }

        span:first-child,
        svg {
          text-shadow: rgb(255, 71, 224, 0.8) 0px 0px 15px;
        }

        svg {
          margin-left: 0.5rem;
          transition: all 100ms ease-in-out;
        }

        &:hover svg {
          transform: translateX(5px);
        }
        &:hover span:first-child {
          transform: translateX(-5px);
        }
      }
    }
  }
}
</style>
