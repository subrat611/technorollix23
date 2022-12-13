<template>
  <div>
    <nav-bar />
    <div class="container">
      <p>site development is in progress...</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CommingSoon',
}
</script>

<style lang="scss" scoped>
.container {
  height: 100vh;
  width: 100vw;
  display: flex;
  justify-content: center;
  align-items: center;
  background: #000;

  p {
    font-family: 'Poppins', sans-serif;
    text-transform: capitalize;
    color: #fff;
    font-size: 1.5rem;
    text-align: center;
    letter-spacing: 0.01em;
  }
}
</style>
