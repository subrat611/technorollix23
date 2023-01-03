<template>
  <div class="main-wrapper">
    <pre-loader v-show="isLoad"></pre-loader>
    <div v-show="!isLoad" class="wrapper">
      <nav-bar />
      <!-- <notify-add v-show="isShowNotif" @close-add="closeAdd" /> -->
      <hero-section />
      <moments-section />
      <junoon-section />
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      isLoad: true,
      isShowNotif: true,
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
    // setTimeout(() => {
    //   this.isLoad = false
    // }, 5000)
  },
  methods: {
    closeAdd() {
      this.isShowNotif = !this.isShowNotif
    },
  },
}
</script>

<style lang="scss" scoped>
.main-wrapper {
  height: 100%;
  width: 100%;
  background: #000;

  .wrapper {
    position: relative;
    padding-bottom: 0.5rem;
  }

  .pride-moment {
    height: 100%;
    width: 100vw;

    .pride-moment-bg {
      // filter: blur(2px);
      position: relative;

      video {
        height: 100%;
        width: 100%;
        transform: rotate(180deg);
      }

      .overlay {
        position: absolute;
        top: 0;
        left: 0;
        height: 100%;
        width: 100%;
        background-image: linear-gradient(
          190deg,
          rgba(201, 37, 107, 0.1) 5.4%,
          rgba(116, 16, 124, 0.1) 74.7%
        );
      }
    }
  }
}
</style>
