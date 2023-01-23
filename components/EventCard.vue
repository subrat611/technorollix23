<template>
  <div class="card-container">
    <div class="card-img"><nuxt-img :src="'/event/' + eventImg" /></div>
    <div class="card-content">
      <p class="card-title">{{ eventName }}</p>
      <p class="card-desc">
        {{ eventDesc }}
        <nuxt-link :to="`/eventdetails/` + eventName.replace(/\s/g, '')"
          >...read more</nuxt-link
        >
      </p>
      <nuxt-link :to="`/eventdetails/` + eventName.replace(/\s/g, '')">
        <button>register</button>
      </nuxt-link>
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
    eventDesc: {
      type: String,
      default:
        'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quasi quisquam fuga, deleniti accusantium neque repudiandae id quos esse in iste. Lorem ipsum dolor sit amet consectetur adipisicing elit',
    },
    eventImg: {
      type: null,
      default: '',
    },
    index: {
      type: Number,
      default: 0,
    },
  },
}
</script>

<style lang="scss" scoped>
a {
  color: #e5e5e5;
}

.card-container {
  margin: 0 0.5rem 4rem 0.5rem;
  width: 400px;
  background: rgba(63, 194, 255, 0.11);
  border-radius: 7px;
  box-shadow: 0 4px 30px rgba(104, 104, 104, 0.1);
  backdrop-filter: blur(3.3px);
  -webkit-backdrop-filter: blur(3.3px);
  border: 1px solid rgba(255, 217, 252, 0.2);
  padding: 1.5rem 1rem;
  display: flex;
  flex-direction: column;
  justify-content: center;

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
      font-family: 'Montserrat', sans-serif;
      font-size: 1.4rem;
      padding: 0.7rem 0;
      font-weight: 600;
      text-transform: capitalize;
    }

    .card-desc {
      line-height: 1.4rem;
      // text-transform: capitalize;
      padding: 0 0.5rem 0 0;
      color: #e5e5e5;
      font-family: 'Montserrat', sans-serif;

      a {
        text-decoration: none;
        font-weight: bold;
        color: #00b4d8;
      }
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
      letter-spacing: 0.02em;
      font-family: 'Montserrat', sans-serif;
      font-weight: 500;
      cursor: pointer;

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
    margin: 1rem 0.2rem;
    padding: 1rem;

    .card-content {
      .card-title {
        font-size: 1.2rem;
      }

      .card-desc {
        font-size: 0.9rem;
        line-height: 1.3rem;
      }

      button {
        font-size: 1rem;
      }
    }
  }
}
</style>
