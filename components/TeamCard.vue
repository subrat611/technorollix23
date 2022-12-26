<template>
  <div class="team-card">
    <nuxt-img src="/1.JPG" />
    <div class="overlay"></div>
  </div>
</template>

<script>
export default {
  name: 'TeamCard',
}
</script>

<style lang="scss" scoped>
.team-card {
  width: 330px;
  height: 350px;
  border: 1px solid red;
  border-radius: 3px;
  margin: 2rem 1rem 1rem 1rem;

  img {
    width: 100%;
  }
}
</style>
