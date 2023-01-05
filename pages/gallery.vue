<template>
  <div>
    <div class="gallery-container">
      <h1 class="page-title">gallery</h1>
      <div class="gallery">
        <div class="gallery-img">
          <nuxt-img
            src="/1.JPG"
            width="520"
            height="320"
            format="webp"
            loading="lazy"
          />
          <nuxt-img
            src="/2.JPG"
            width="550"
            height="360"
            format="webp"
            loading="lazy"
          />
        </div>
        <div class="gallery-img">
          <nuxt-img
            src="/3.JPG"
            width="550"
            height="360"
            format="webp"
            loading="lazy"
          />
          <nuxt-img
            src="/4.JPG"
            width="550"
            height="360"
            format="webp"
            loading="lazy"
          />
        </div>
        <div class="gallery-img">
          <nuxt-img
            src="/5.JPG"
            width="550"
            height="360"
            format="webp"
            loading="lazy"
          />
          <nuxt-img
            src="/6.JPG"
            width="550"
            height="360"
            format="webp"
            loading="lazy"
          />
        </div>
        <div class="gallery-img">
          <nuxt-img
            src="/7.JPG"
            width="550"
            height="360"
            format="webp"
            loading="lazy"
          />
          <nuxt-img
            src="/8.JPG"
            width="550"
            height="360"
            format="webp"
            loading="lazy"
          />
        </div>
        <div class="gallery-img">
          <nuxt-img
            src="/9.JPG"
            width="550"
            height="360"
            format="webp"
            loading="lazy"
          />
          <nuxt-img
            src="/10.JPG"
            width="550"
            height="360"
            format="webp"
            loading="lazy"
          />
        </div>
        <div class="gallery-img">
          <nuxt-img
            src="/11.JPG"
            width="550"
            height="360"
            format="webp"
            loading="lazy"
          />
          <nuxt-img
            src="/12.jpg"
            width="550"
            height="360"
            format="webp"
            loading="lazy"
          />
        </div>
        <div class="gallery-img">
          <nuxt-img
            src="/13.jpg"
            width="550"
            height="360"
            format="webp"
            loading="lazy"
          />
          <nuxt-img
            src="/14.jpg"
            width="550"
            height="360"
            format="webp"
            loading="lazy"
          />
        </div>
        <div class="gallery-img">
          <nuxt-img
            src="/15.jpg"
            width="550"
            height="360"
            format="webp"
            loading="lazy"
          />
          <nuxt-img
            src="/16.jpg"
            width="550"
            height="360"
            format="webp"
            loading="lazy"
          />
        </div>
        <div class="gallery-img">
          <nuxt-img
            src="/17.jpg"
            width="550"
            height="360"
            format="webp"
            loading="lazy"
          />
          <nuxt-img
            src="/18.jpg"
            width="550"
            height="360"
            format="webp"
            loading="lazy"
          />
        </div>
      </div>
    </div>
    <nav-bar />
  </div>
</template>

<script>
export default {
  name: 'GalleryPage',
}
</script>

<style lang="scss" scoped>
.gallery-container {
  background: #000;
  color: #fff;
  height: 100vh;
  width: 100vw;
  overflow: hidden scroll;

  &::-webkit-scrollbar {
    width: 0;
  }

  .page-title {
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    font-size: 5rem;
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
    padding: 2rem 0;
    .gallery-img {
      height: 70vh;
      display: flex;
      justify-content: space-around;
      padding: 1.5rem 0 1rem 0;

      img:nth-child(2) {
        align-self: flex-end;
        border-radius: 4px;
      }
    }
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
