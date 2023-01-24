<template>
  <div class="team-card-container">
    <div class="card">
      <event-detail v-for="(member, i) in teams" :key="i" :member="member" />
    </div>
  </div>
</template>

<script>
export default {
  name: 'EventDetails',
  props: {
    teams: {
      type: Array,
      default: null,
    },
  },
}
</script>

<style lang="scss" scoped>
.team-card-container {
  margin-top: 1rem;
  .card {
    display: flex;
    flex-wrap: wrap;
    justify-content: flex-start;
  }
}

@media all and (max-width: '912px') {
  .team-card-container {
    .card {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-around;
    }
  }
}
</style>
