<template>
  <div class="wrapper" @click="$router.go(-1)">
    <svg
      xmlns="http://www.w3.org/2000/svg"
      class="ionicon"
      viewBox="0 0 512 512"
    >
      <title>Arrow Back</title>
      <path
        fill="none"
        stroke="currentColor"
        stroke-linecap="round"
        stroke-linejoin="round"
        stroke-width="48"
        d="M244 400L100 256l144-144M120 256h292"
      />
    </svg>
  </div>
</template>

<script>
export default {
  name: 'BackBtn',
}
</script>

<style lang="scss" scoped>
.wrapper {
  position: absolute;
  top: 2%;
  left: 2%;
  width: fit-content;
  padding: 0.6rem;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 50%;

  background: rgba(42, 157, 143, 0.57);
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
  backdrop-filter: blur(4.5px);
  -webkit-backdrop-filter: blur(4.5px);
  border: 1px solid rgba(42, 157, 143, 0.3);

  &:hover {
    background: rgba(42, 157, 144, 0.603);
    cursor: pointer;
  }

  svg {
    height: 26px;
    color: #ffffff;
  }
}
</style>
