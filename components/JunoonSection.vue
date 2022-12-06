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
        <p class="title">Junoon</p>
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

      span:first-child {
        text-shadow: rgba(255, 0, 193, 1) 0px 0px 15px,
          rgba(255, 0, 193, 0.5) 0px 0px 10px;
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

@media (max-width: '360px') {
  .junoon-section {
    .hero-text {
      .title {
        font-size: 4.8rem;
      }
      .reg-btn {
        margin-top: 9rem;
      }
    }
  }
}
</style>
