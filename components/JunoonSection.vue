<template>
  <div class="junoon-section">
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
        <p class="title">GRAND DJ</p>
      </div>
      <!-- <div class="reg-btn">
        <span>Get ticket</span>
      </div> -->
    </div>
  </div>
</template>

<script>
export default {
  name: 'JunoonSection',
}
</script>

<style lang="scss" scoped>
.junoon-section {
  width: 100%;
  height: 100vh;
  position: relative;
  background: #000;

  .hero-img {
    height: 100%;
    display: flex;
    position: relative;

    .darshan-img,
    .jubin-img,
    .shirely-img {
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
      opacity: 0.3;
      background-image: linear-gradient(
        109.6deg,
        rgba(45, 116, 213, 1) 11.2%,
        rgba(121, 137, 212, 1) 91.2%
      );
      background: #ff0084; /* fallback for old browsers */
      background: -webkit-linear-gradient(
        to left,
        #33001b,
        #ff0084
      ); /* Chrome 10-25, Safari 5.1-6 */
      background: linear-gradient(
        to left,
        #33001b,
        #ff0084
      ); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
      background-image: radial-gradient(
        circle 610px at 5.2% 51.6%,
        rgba(5, 8, 114, 1) 0%,
        rgba(7, 3, 53, 1) 97.5%
      );
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

    .title {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      font-size: 11rem;
      font-family: 'adobo';
      text-transform: uppercase;
      letter-spacing: 0.08em;
      color: #ffffcb;
      z-index: 2;
      text-shadow: rgba(255, 247, 94, 1) 0px 0px 24px,
        rgba(255, 247, 94, 1) 0px 0px 15px;
      &::selection {
        background: none;
      }
    }

    .reg-btn {
      display: flex;
      align-items: center;
      margin-top: 15rem;
      cursor: pointer;

      span:first-child {
        font-family: 'Poppins', sans-serif;
        font-weight: 400;
        font-size: 1.3rem;
        letter-spacing: 0.02em;
        transition: all 100ms ease-in-out;

        padding: 0.6em 1.7rem;
        background: rgba(255, 125, 252, 0.12);
        border-radius: 3px;
        box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
        backdrop-filter: blur(3.3px);
        -webkit-backdrop-filter: blur(3.3px);
        border: 1px solid rgba(255, 125, 252, 0.26);
        color: #fff;
        text-shadow: rgba(255, 0, 193, 0.5) 0px 0px 10px,
          rgba(255, 0, 193, 0.5) 0px 0px 10px;

        &::selection {
          background: none;
        }

        &:hover {
          background: rgba(255, 125, 252, 0.22);
        }
      }
    }
  }
}

@media (max-width: '912px') {
  .junoon-section {
    .hero-text {
      .title {
        font-size: 4.8rem;
      }
      .reg-btn {
        margin-top: 9rem;

        span:first-child {
          font-size: 1.05rem;
        }
      }
    }

    .hero-img {

      .jubin-img {
        img {
          object-position: center center;
        }
      }

      .shirely-img {
        img {
          object-position: 30% center;
        }
      }
    }
  }
}
</style>
