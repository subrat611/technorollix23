<template>
  <div class="pride-moments">
    <div class="pride-moment-bg">
      <!-- <img src="~/assets/img/bg-1.jpg" alt="" srcset="" /> -->
      <video pause muted src="~/assets/videos/3d-bg.mp4"></video>
      <div class="overlay"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MomentsSection',
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

    video {
      filter: blur(1.3px);
      position: absolute;
      top: 0;
      left: 0;
      height: 100%;
      width: 100%;
      object-fit: cover;
      transform: rotate(180deg);
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
}
</style>
