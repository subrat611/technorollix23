<template>
  <div class="team-card">
    <nuxt-img :src="'/team/' + member.image" format="webp" loading="lazy" />
    <div class="overlay">
      <p class="title">{{ member.name }}</p>
      <p class="desig">{{ member.designation }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TeamCard',
  props: {
    member: {
      type: Object,
      default: null,
    },
  },
}
</script>

<style lang="scss" scoped>
.team-card {
  width: 280px;
  height: 350px;
  border-radius: 3px;
  margin: 2rem 1rem 1rem 1rem;
  background: #edf2f4;
  position: relative;
  background-image: radial-gradient(
    circle 941px at 2.6% 6.8%,
    rgba(228, 214, 24, 0.81) 15.9%,
    rgba(249, 208, 40, 0.7) 88.6%
  );

  img {
    width: 100%;
    height: 100%;
    transition: transform 200ms cubic-bezier(0.68, -0.55, 0.27, 1.55);
  }

  .overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    // background: rgba(73, 160, 120, 0.8);
    background-image: radial-gradient(
      circle farthest-corner at 10% 20%,
      rgba(0, 152, 155, 0.9) 3.1%,
      rgba(0, 94, 120, 0.8) 94.2%
    );
    color: #fff;
    padding: 2rem 0.5rem;
    transition: all 300ms ease-in-out;

    .title {
      color: #ffffff;
      font-family: 'Montserrat', sans-serif;
      font-weight: bolder;
      letter-spacing: 0.05em;
      font-size: 1.6rem;
      text-shadow: rgb(241, 241, 241) 0px 0px 1px,
        rgba(211, 211, 211, 0.568) 0px 0px 2px;
    }

    .desig {
      padding-top: 1rem;
      font-family: 'Montserrat', sans-serif;
      font-weight: bolder;
      letter-spacing: 0.08em;
      font-size: 1rem;
      text-shadow: rgb(241, 241, 241) 0px 0px 1px,
        rgba(216, 216, 216, 0.568) 0px 0px 2px;
    }
  }

  &:hover {
    overflow: hidden;

    img {
      transform: scale(1.02);
    }
    .overlay {
      opacity: 0;
    }
  }
}
</style>
