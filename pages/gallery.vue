<template>
  <div>
    <nav-bar />
    <nav-bar-two />
    <div class="gallery-container">
      <h1 class="page-title">gallery</h1>
      <div class="gallery">
        <div class="gallery-img">
          <nuxt-img src="/1.JPG" loading="lazy" />
          <nuxt-img src="/2.JPG" loading="lazy" />
        </div>
        <div class="gallery-img">
          <nuxt-img src="/3.JPG" loading="lazy" />
          <nuxt-img src="/4.JPG" loading="lazy" />
        </div>
        <div class="gallery-img">
          <nuxt-img src="/5.JPG" loading="lazy" />
          <nuxt-img src="/6.JPG" loading="lazy" />
        </div>
        <div class="gallery-img">
          <nuxt-img src="/7.JPG" loading="lazy" />
          <nuxt-img src="/8.JPG" loading="lazy" />
        </div>
        <div class="gallery-img">
          <nuxt-img src="/9.JPG" loading="lazy" />
          <nuxt-img src="/10.JPG" loading="lazy" />
        </div>
        <div class="gallery-img">
          <nuxt-img src="/11.JPG" loading="lazy" />
          <nuxt-img src="/12.jpg" loading="lazy" />
        </div>
        <div class="gallery-img">
          <nuxt-img src="/13.jpg" loading="lazy" />
          <nuxt-img src="/14.jpg" loading="lazy" />
        </div>
        <div class="gallery-img">
          <nuxt-img src="/15.jpg" loading="lazy" />
          <nuxt-img src="/16.jpg" loading="lazy" />
        </div>
        <div class="gallery-img">
          <nuxt-img src="/17.jpg" loading="lazy" />
          <nuxt-img src="/18.jpg" loading="lazy" />
        </div>
      </div>
    </div>
    <nav-bar />
    <nav-bar-three />
  </div>
</template>

<script>
export default {
  name: 'GalleryPage',
}
</script>

<style lang="scss" scoped>
.gallery-container {
  padding-top: 6rem;
  background: #000;
  color: #fff;
  height: 100vh;
  width: 100vw;
  overflow: hidden scroll;

  &::-webkit-scrollbar {
    width: 0;
  }

  .page-title {
    // position: fixed;
    // top: 50%;
    // left: 50%;
    // transform: translate(-50%, -50%);
    margin: 3rem 0 2rem 0;
    text-align: center;
    font-size: 4rem;
    text-transform: uppercase;
    font-family: 'Montserrat', sans-serif;
    font-weight: 800;
    letter-spacing: 0.1em;
    text-shadow: rgb(170, 169, 169) 0px 0px 10px,
      rgb(187, 187, 187) 0px 0px 14px;
    pointer-events: none;

    &::selection {
      background: none;
    }
  }

  .gallery {
    padding: 1rem 0;
    margin-bottom: 5rem;
    .gallery-img {
      height: 55vh;
      display: flex;
      justify-content: space-evenly;
      padding: 1.5rem 0 1rem 0;

      img {
        width: 550px;
        height: 353px;
        border-radius: 7px;
        // box-shadow: rgba(181, 181, 182, 0.384) 0px 8px 24px;
        box-shadow: rgba(40, 31, 92, 0.685) 0px 48px 100px 0px;
      }
      img:nth-child(2) {
        align-self: flex-end;
        border-radius: 4px;
      }
    }
  }
}

@media all and (max-width: '1248px') {
  .gallery-container {
    padding-top: 0;
  }
}

@media all and (max-width: '912px') {
  .gallery-container {
    .page-title {
      font-size: 1.5rem;
      z-index: 2;
    }

    .gallery {
      .gallery-img {
        height: 63vh;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        padding: 0.5rem 0;

        img {
          width: 320px;
          height: 232px;
          margin-top: 1rem;
        }
        img:nth-child(2) {
          align-self: center;
        }
      }
    }
  }
}
</style>
