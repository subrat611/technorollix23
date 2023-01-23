<template>
  <div class="home-logo-wrapper">
    <div class="logo-container">
      <nuxt-img src="/technorollixlogo.png" class="logo" format="webp" />
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeLogoTop',
}
</script>

<style lang="scss" scoped>
.home-logo-wrapper {
  display: none;
  position: fixed;
  top: 0;
  left: 50%;
  transform: translate(-50%);
  z-index: 1;

  .logo-container {
    background: rgba(23, 2, 73, 0.5);
    border-radius: 0 0 16px 16px;
    box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
    backdrop-filter: blur(5.5px);
    -webkit-backdrop-filter: blur(5.5px);
    padding: 0.2rem 0;

    .logo {
      padding: 0 1rem;
      width: 156px;
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
