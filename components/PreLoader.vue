<template>
  <div class="loading-screen">
    <video
      ref="bg_video"
      autoplay
      loop
      muted
      src="~/assets/videos/loding-video.mp4"
    ></video>
  </div>
</template>

<script>
export default {
  name: 'PreLoader',
}
</script>

<style lang="scss" scoped>
.loading-screen {
  height: 100vh;
  width: 100%;
  background: #000;
  display: flex;
  justify-content: center;
  align-items: center;

  video {
    height: 50%;
    width: 50%;
  }
}
</style>
