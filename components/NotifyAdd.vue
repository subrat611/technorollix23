<template>
  <div>
    <div class="addvert">
      <p>site development is in progress</p>
      <p class="cross-btn" @click="$emit('close-add')">X</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'NotifyAdd',
}
</script>

<style lang="scss" scoped>
.addvert {
  width: 100vw;
  position: relative;
  background-image: linear-gradient(
    109.6deg,
    rgba(24, 138, 141, 1) 11.2%,
    rgba(96, 221, 142, 1) 91.1%
  );

  p {
    width: 80%;
    margin: 0 auto;
    padding: 0.7rem 0.3rem;
    text-align: center;
    color: #fff;
    font-family: 'Poppins', sans-serif;
    text-transform: capitalize;
    font-size: 1.01rem;
  }

  .cross-btn {
    width: fit-content;
    position: absolute;
    top: 50%;
    right: 2%;
    transform: translate(-50%, -50%);
    cursor: pointer;
    font-weight: 600;
    color: #42033d;
  }
}
</style>
