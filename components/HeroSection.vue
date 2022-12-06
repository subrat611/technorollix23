<template>
  <div class="hero-wrapper">
    <div class="bg-video">
      <video
        autoplay
        loop
        muted
        src="~/assets/videos/hero-bg-video.mp4"
      ></video>
    </div>
    <div class="content">
      <p class="techno-title">TECHNOROLLIX</p>
      <p class="techno-sub">2023</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HeroSection',
}
</script>

<style lang="scss" scoped>
.hero-wrapper {
  height: 100vh;
  width: 100vw;
  position: relative;

  .bg-video {
    height: 100%;
    width: 100vw;
    position: relative;

    video {
      position: absolute;
      top: 0;
      left: 0;
      height: 100%;
      width: 100%;
      object-fit: cover;
    }
  }

  .content {
    position: absolute;
    top: 0;
    left: 0;
    height: 100%;
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    .techno-title {
      font-size: 7rem;
      color: #fff;
      font-weight: 800;
      // font-family: 'Montserrat', sans-serif;
      font-family: 'origin Tech';
      letter-spacing: 0.1em;
      text-shadow: rgb(255, 120, 239, 0.5) 0px 0px 15px,
        rgb(255, 120, 239, 0.5) 0px 0px 15px, rgb(255, 120, 239, 1) 0px 0px 15px;
    }

    .techno-sub {
      margin-top: 1rem;
      text-align: center;
      color: #fff;
      font-size: 5.6rem;
      font-family: 'origin Tech';
      text-shadow: rgba(91, 212, 247, 1) 0px 0px 15px,
        rgba(91, 212, 247, 1) 0px 0px 15px, rgba(91, 212, 247, 1) 0px 0px 15px;
    }
  }
}
</style>
