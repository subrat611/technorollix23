<template>
  <div class="card-container">
    <div class="card-img">
      <img src="~/assets/img/bg.png" />
    </div>
    <div class="card-content">
      <p class="card-title">{{ eventName }}</p>
      <p class="card-desc">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Quasi quisquam
        fuga, deleniti accusantium neque repudiandae id quos esse in iste.
      </p>
      <button>register</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'EventCard',
  props: {
    eventName: {
      type: String,
      default: 'Event name',
    },
  },
}
</script>

<style lang="scss" scoped>
.card-container {
  margin: 0 0.5rem 4rem 0.5rem;
  width: 400px;
  background: rgba(63, 194, 255, 0.11);
  border-radius: 7px;
  box-shadow: 0 4px 30px rgba(104, 104, 104, 0.1);
  backdrop-filter: blur(3.3px);
  -webkit-backdrop-filter: blur(3.3px);
  border: 1px solid rgba(255, 217, 252, 0.2);
  padding: 1rem;

  .card-img {
    width: 100%;

    img {
      border-radius: 6px;
      width: 100%;
    }
  }
  .card-content {
    width: 100%;

    .card-title {
      font-size: 1.4rem;
      padding: 0.7rem 0;
      font-weight: 600;
      text-transform: capitalize;
    }

    .card-desc {
      line-height: 1.2rem;
      text-transform: capitalize;
      padding: 0 1rem 0 0;
    }

    button {
      margin-top: 1rem;
      width: 100%;
      padding: 0.7rem;
      font-size: 1.2rem;
      border: none;
      color: #fff;
      text-transform: capitalize;
      border-radius: 3px;
      outline: none;
      letter-spacing: 0.05em;

      background: rgba(255, 255, 255, 0.116);
      box-shadow: 0 4px 30px rgba(255, 255, 255, 0.1);
      backdrop-filter: blur(3.3px);
      -webkit-backdrop-filter: blur(3.3px);

      transition: all 200ms ease-out;

      &:hover {
        background: rgba(255, 255, 255, 0.253);
        box-shadow: 0 4px 30px rgba(255, 255, 255, 0.1);
        backdrop-filter: blur(3.3px);
        -webkit-backdrop-filter: blur(3.3px);
      }
    }
  }
}

@media all and (max-width: '912px') {
  .card-container {
    width: 100%;
    margin: 1rem 0.5rem;

    .card-content {
      p:first-child {
        font-size: 1.1rem;
      }

      p:last-child {
        font-size: 1rem;
      }

      button {
        font-size: 1rem;
      }
    }
  }
}
</style>
