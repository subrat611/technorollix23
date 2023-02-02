<template>
  <div class="home-logo-wrapper" :class="{ 'navbar-hidden': !showNavbar }">
    <div class="logo-container">
      <!-- <nuxt-img src="/technorollixlogo.png" class="logo" format="webp" /> -->
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeLogoBottom',
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
.home-logo-wrapper {
  display: none;
  position: fixed;
  bottom: 0%;
  left: 50%;
  transform: translate(-50%);
  z-index: 1;

  &.navbar-hidden {
    transform: translate3d(0, -100vh, 0);
    display: none;
  }

  .logo-container {
    background: rgba(23, 2, 73, 0.5);
    border-radius: 16px 16px 0 0;
    box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
    backdrop-filter: blur(5.5px);
    -webkit-backdrop-filter: blur(5.5px);
    padding: 0.3rem 0;

    .logo {
      padding: 0 1rem;
      width: 154px;
      filter: drop-shadow(0 3px 30px rgba(220, 100, 20, 0.8));
    }
  }
}

@media all and (max-width: '1248px') {
  .home-logo-wrapper {
    display: block;
  }
}
</style>
