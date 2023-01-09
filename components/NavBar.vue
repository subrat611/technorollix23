<template>
  <div>
    <div class="nav-container" @click="openMenu">
      <div class="nav-bar">
        <div :class="toggleMenu ? 'bar-one-click' : 'bar-one'"></div>
        <div :class="toggleMenu ? 'bar-two-click' : 'bar-two'"></div>
        <div :class="toggleMenu ? 'bar-three-click' : 'bar-three'"></div>
      </div>
    </div>
    <div v-show="toggleMenu" class="nav-content">
      <div class="nav-items-content">
        <ul class="nav-items">
          <li class="nav-item" @click="openMenu">
            <nuxt-link to="/">home</nuxt-link>
          </li>
          <li class="nav-item" @click="openMenu">
            <nuxt-link to="/event">events</nuxt-link>
          </li>
          <li class="nav-item" @click="openMenu">
            <nuxt-link to="/commingsoon">schedule</nuxt-link>
          </li>
          <li class="nav-item" @click="openMenu">
            <nuxt-link to="/team">team</nuxt-link>
          </li>
          <li class="nav-item" @click="openMenu">
            <nuxt-link to="/gallery">gallery</nuxt-link>
          </li>
          <li class="nav-item" @click="openMenu">
            <nuxt-link to="/aboutus">about us</nuxt-link>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'NavBar',
  data() {
    return {
      toggleMenu: false,
    }
  },
  methods: {
    openMenu() {
      this.toggleMenu = !this.toggleMenu
    },
  },
}
</script>

<style lang="scss" scoped>
.nav-container {
  position: fixed;
  bottom: 3%;
  right: 5%;
  z-index: 4;

  .nav-bar {
    /* From https://css.glass */
    background: rgba(42, 157, 143, 0.57);
    border-radius: 16px;
    box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
    backdrop-filter: blur(4.5px);
    -webkit-backdrop-filter: blur(4.5px);
    border: 1px solid rgba(42, 157, 143, 0.3);

    // box-shadow: rgba(0, 0, 0, 0.1) 0px 4px 12px;
    // background-color: #131515;
    height: 50px;
    width: 50px;
    border-radius: 50%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    div {
      width: 26px;
      height: 2px;
      background: #fff;
      padding: 1.6px 0;
      margin: 0.15rem 0;
      border-radius: 3px;
      transition: all 0.4s cubic-bezier(0.68, -0.6, 0.32, 1.6);
    }

    .bar-one-click {
      transform: rotate(45deg) translate(5px, 6px);
    }

    .bar-two-click {
      transform: translate(15px);
      opacity: 0;
    }

    .bar-three-click {
      transform: rotate(-45deg) translate(6px, -6px);
    }
  }
}

.nav-content {
  position: fixed;
  top: 0;
  left: 0;
  background: #000;
  z-index: 3;
  height: 100vh;
  width: 100vw;
  animation: toggle-menu 0.6s cubic-bezier(0.65, 0.05, 0.36, 1) forwards
    alternate;

  .nav-items-content {
    height: 100%;
    width: 100%;
    .nav-items {
      padding-top: 2rem;
      height: 80%;
      width: inherit;
      display: flex;
      flex-direction: column;
      justify-content: space-around;
      padding-left: 1.6rem;

      .nav-item {
        animation: fade-in 0.8s cubic-bezier(0.65, 0.05, 0.36, 1);
        a {
          color: #fff;
          text-decoration: none;
          text-transform: uppercase;
          font-size: 3rem;
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
          scale: 1.04;
        }
      }
    }
  }
}

@keyframes toggle-menu {
  0% {
    position: fixed;
    top: 0;
    height: 10vh;
    width: 100%;
  }
  100% {
    height: 100vh;
    width: 100vw;
  }
}

@keyframes fade-in {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}

@media (max-width: '912px') {
  .nav-content {
    .nav-items-content {
      .nav-items {
        display: block;
        padding-top: 1.5rem;

        .nav-item {
          padding: 1.5rem 0;
          a {
            font-size: 2.5rem;
          }
        }
      }
    }
  }
}
</style>
