<template>
  <div class="nav-container" @click="openMenu">
    <div class="nav-bar">
      <div :class="toggleMenu ? 'bar-one-click' : 'bar-one'"></div>
      <div :class="toggleMenu ? 'bar-two-click' : 'bar-two'"></div>
      <div :class="toggleMenu ? 'bar-three-click' : 'bar-three'"></div>
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
  z-index: 1;

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
</style>
