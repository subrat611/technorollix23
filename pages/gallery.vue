<template>
  <div class="gallery-container">
    <h1 class="page-title">gallery page</h1>
    
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

    &::selection {
      background: none;
    }
  }
}
</style>
