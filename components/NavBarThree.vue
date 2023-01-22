<template>
  <div>
    <div class="nav-container" :class="{ 'navbar-hidden': !showNavbar }">
      <div class="nav-content">
        <div class="nav-items-left">
          <ul class="nav-items">
            <li class="nav-item">
              <nuxt-link to="/team">contact us</nuxt-link>
            </li>
            <li class="nav-item">
              <nuxt-link to="/event">about us</nuxt-link>
            </li>
            <li class="nav-item">
              <nuxt-link to="/commingsoon">sponsors</nuxt-link>
            </li>
          </ul>
        </div>
        <div class="nav-items-center">
          <nuxt-img src="/technorollixlogo.png" class="logo" format="webp" />
        </div>
        <div class="nav-items-right">
          <ul class="nav-items">
            <li class="nav-item">
              <nuxt-link to="/team">
                <nuxt-img src="/pinterest.png" format="webp" width="35" />
              </nuxt-link>
            </li>
            <li class="nav-item">
              <nuxt-link to="/gallery">
                <nuxt-img src="/instagram.png" format="webp" width="35" />
              </nuxt-link>
            </li>
            <li class="nav-item">
              <nuxt-link to="/aboutus">
                <nuxt-img src="/facebook.png" format="webp" width="35" />
              </nuxt-link>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'NavBarTwo',
  data() {
    return {
      showNavbar: true,
      lastScrollPosition: 0,
    }
  },
  mounted() {
    window.addEventListener('scroll', this.onScroll)
  },
  beforeDestroy() {
    window.removeEventListener('scroll', this.onScroll)
  },
  methods: {
    onScroll() {
      const currentScrollPosition =
        window.pageYOffset || document.documentElement.scrollTop
      if (currentScrollPosition < 0) {
        return
      }
      // Stop executing this function if the difference between
      // current scroll position and last scroll position is less than some offset
      if (Math.abs(currentScrollPosition + this.lastScrollPosition) < 60) {
        return
      }
      this.showNavbar = currentScrollPosition < this.lastScrollPosition
      this.lastScrollPosition = currentScrollPosition
    },
  },
}
</script>

<style lang="scss" scoped>
.nav-container {
  position: fixed;
  bottom: 0;
  left: 0;
  z-index: 4;
  width: 100vw;
  transform: translate3d(0, 0, 0);
  transition: 0.1s all ease-out;
  background-image: linear-gradient(
    to bottom,
    rgba(15, 15, 15, 0),
    rgba(0, 0, 0, 0.849)
  );
  padding: 1.3rem 0;

  &.navbar-hidden {
    transform: translate3d(0, -100%, 0);
    display: none;
  }

  .nav-content {
    // height: 80px;
    // border: 1px solid red;
    display: flex;
    justify-content: space-around;
    align-items: center;

    .nav-items-left {
      position: relative;
      width: 545px;
      height: 70px;
      &::before {
        content: '';
        position: absolute;
        top: 0;
        left: 0;
        height: 100%;
        width: 100%;
        background-image: linear-gradient(
          -43.2deg,
          rgba(13, 6, 26, 0.712) 10.8%,
          rgba(236, 13, 117, 0.521) 94.3%
        );
        box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
        backdrop-filter: blur(2.8px);
        -webkit-backdrop-filter: blur(5.8px);
        transform: skewX(-200deg);
      }
    }

    .nav-items-center {
      /* From https://css.glass */
      background: rgba(35, 9, 51, 0.66);
      border-radius: 16px 16px 0 0;
      box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
      backdrop-filter: blur(6.5px);
      -webkit-backdrop-filter: blur(6.5px);

      .logo {
        padding: 0 1rem;
        width: 200px;
        filter: drop-shadow(0 3px 30px rgba(220, 100, 20, 0.8));
      }
    }

    .nav-items-right {
      position: relative;
      width: 545px;
      height: 70px;

      &::before {
        content: '';
        position: absolute;
        top: 0;
        left: 0;
        height: 100%;
        width: 100%;
        background-image: linear-gradient(
          43.2deg,
          rgba(13, 6, 26, 0.712) 10.8%,
          rgba(236, 13, 117, 0.521) 94.3%
        );
        box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
        backdrop-filter: blur(2.8px);
        -webkit-backdrop-filter: blur(5.8px);
        transform: skewX(200deg);
      }
    }

    .nav-items-left,
    .nav-items-center,
    .nav-items-right {
      padding: 0.8rem 0;
    }

    h2 {
      color: #fff;
    }

    .nav-items {
      display: flex;
      justify-content: space-around;
      padding: 0.5rem;

      .nav-item {
        padding: 0 1.2rem;
        animation: fade-in 0.8s cubic-bezier(0.65, 0.05, 0.36, 1);
        a {
          color: #fff;
          text-decoration: none;
          text-transform: uppercase;
          font-size: 1.3rem;
          font-family: 'Montserrat', sans-serif;
          font-weight: 800;
          letter-spacing: 0.06em;
          transition: color 0.3s ease-in-out;

          &:hover {
            color: aqua;
          }
        }

        width: fit-content;
        transition: scale 0.3s ease-in-out;
        scale: 1;

        &:hover {
          scale: 1.02;
        }
      }
    }
  }
}

@media all and (max-width: '1248px') {
  .nav-container {
    display: none;
  }
}
</style>
