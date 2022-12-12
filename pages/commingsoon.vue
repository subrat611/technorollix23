<template>
  <div>
    <nav-bar />
    <div class="container">
      <h1>comming soon</h1>
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

  h1 {
    font-family: 'adobo';
    text-transform: uppercase;
    color: #fff;
    font-size: 3rem;
    text-align: center;
    letter-spacing: 0.2em;
  }
}
</style>
