<template>
  <div>
    <nav-bar />
    <div class="container">
      <h1>Registration open very soon....</h1>
    </div>
  </div>
</template>

<script>
export default {
  name: 'RegisterPage',
}
</script>

<style lang="scss" scoped>
.container {
  background: #000;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;

  h1 {
    padding: 0 1rem;
    color: #fff;
    font-family: 'Poppins', sans-serif;
    letter-spacing: 0.05em;
    text-align: center;
  }
}
</style>
