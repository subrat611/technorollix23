<template>
  <div class="pride-moments">
    <div class="pride-moment-bg">
      <img src="~/assets/img/bg.png" alt="background" />
      <div class="overlay"></div>
    </div>
    <div class="content">
      <div class="main-text">
        <span class="title">Our Pride Moments</span>
      </div>
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

    img {
      filter: blur(1.3px);
      position: absolute;
      top: 0;
      left: 0;
      height: 100%;
      width: 100%;
      object-fit: cover;
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

  .content {
    position: absolute;
    height: 100%;
    width: 100%;
    top: 0;
    left: 0;

    .main-text {
      height: 100%;
      width: 100%;
      display: flex;
      justify-content: center;
      align-items: center;

      .title {
        color: #fff;
        font-size: 6.2rem;
        font-family: 'Montserrat', sans-serif;
        font-weight: 700;
      }
    }
  }
}

@media (max-width: '360px') {
  .pride-moments {
    .content {
      .main-text {
        .title {
          font-size: 2rem;
        }
      }
    }
  }
}
</style>
