<template>
  <div class="event-details-wrapper">
    <back-btn />
    <div class="detail-container">jaf</div>
  </div>
</template>

<script>
export default {
  name: 'EventDetailsPage',
  data() {
    return {
      a: 1,
    }
  },
  created() {
    this.a = 2
    console.log(this.a)
  },
}
</script>

<style lang="scss" scoped>
.event-details-wrapper {
  background: #000;
  padding: 2rem 0.5rem 1rem 0.5rem;
  color: #fff;
  min-height: 100vh;
  max-height: 100%;
  background-image: linear-gradient(to bottom, #600f634f, #58014059);
}
</style>
