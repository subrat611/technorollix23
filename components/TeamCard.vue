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
  width: 275px;
  height: 370px;
  border-radius: 3px;
  margin: 2rem 1rem 1rem 1rem;
  background: #edf2f4;
  position: relative;
  background: #000;
  background-image: radial-gradient(
    circle farthest-corner at 1.1% 2.5%,
    rgba(0, 113, 208, 1) 0%,
    rgba(0, 160, 247, 1) 24%,
    rgb(140, 2, 175) 71.9%
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
    background: rgba(7, 7, 7, 0.5);
    background-image: linear-gradient(
      178.8deg,
      rgba(0, 88, 143, 0.233) 13.8%,
      rgba(21, 189, 240, 0.103) 95.4%
    );
    color: #fff;
    padding: 2rem 0.5rem;
    transition: all 300ms ease-in-out;

    .title {
      position: absolute;
      bottom: 12%;
      color: #ffffff;
      font-family: 'Montserrat', sans-serif;
      font-weight: bolder;
      letter-spacing: 0.05em;
      font-size: 1.6rem;
      text-shadow: rgb(241, 241, 241) 0px 0px 1px,
        rgba(211, 211, 211, 0.712) 0px 0px 2px;
      padding: 0 0.5rem;
    }

    .desig {
      position: absolute;
      bottom: 5%;
      padding: 1rem 0.5rem 0rem 0.5rem;
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
