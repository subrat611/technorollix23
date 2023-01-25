<template>
  <div class="team-wrapper">
    <div class="img-container">
      <nuxt-img
        :src="'/event_contact/' + member.img"
        format="webp"
        loading="lazy"
      />
    </div>
    <div class="member-contact">
      <p class="member-title">{{ member.name }}</p>
      <div class="contact-links">
        <a v-if="member.call" :href="'tel:+91' + member.call" style="color: black">
          <div class="contact">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="ionicon"
              viewBox="0 0 512 512"
            >
              <title>Call</title>
              <path
                d="M451 374c-15.88-16-54.34-39.35-73-48.76-24.3-12.24-26.3-13.24-45.4.95-12.74 9.47-21.21 17.93-36.12 14.75s-47.31-21.11-75.68-49.39-47.34-61.62-50.53-76.48 5.41-23.23 14.79-36c13.22-18 12.22-21 .92-45.3-8.81-18.9-32.84-57-48.9-72.8C119.9 44 119.9 47 108.83 51.6A160.15 160.15 0 0083 65.37C67 76 58.12 84.83 51.91 98.1s-9 44.38 23.07 102.64 54.57 88.05 101.14 134.49S258.5 406.64 310.85 436c64.76 36.27 89.6 29.2 102.91 23s22.18-15 32.83-31a159.09 159.09 0 0013.8-25.8C465 391.17 468 391.17 451 374z"
                fill="none"
                stroke="currentColor"
                stroke-miterlimit="10"
                stroke-width="32"
              />
            </svg>
          </div>
        </a>
        <a
          v-if="member.mail"
          :href="'mailto:' + member.mail"
          style="color: black"
        >
          <div v-if="member.mail" class="contact">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="ionicon"
              viewBox="0 0 512 512"
            >
              <title>Mail</title>
              <rect
                x="48"
                y="96"
                width="416"
                height="320"
                rx="40"
                ry="40"
                fill="none"
                stroke="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="32"
              />
              <path
                fill="none"
                stroke="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="32"
                d="M112 160l144 112 144-112"
              />
            </svg>
          </div>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'EventDetail',
  props: {
    member: {
      type: Object,
      default: null,
    },
  },
}
</script>

<style lang="scss" scoped>
.team-wrapper {
  width: 200px;
  margin: 1rem;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  .img-container {
    height: 164px;
    width: 164px;
    border-radius: 50%;

    img {
      height: 100%;
      width: 100%;
      border-radius: 50%;
    }
  }

  .member-contact {
    margin: 1rem 0;

    .member-title {
      font-family: 'Roboto', sans-serif;
      font-weight: 500;
      font-size: 1.2rem;
      letter-spacing: 0.05rem;
      text-align: center;
    }

    .contact-links {
      margin-top: 0.6rem;
      display: flex;
      justify-content: space-evenly;
      align-items: flex-end;

      .contact {
        height: 35px;
        width: 35px;
        background: #fff;
        border-radius: 12px;
        padding: 1rem;
        position: relative;
        cursor: pointer;

        svg {
          position: absolute;
          top: 50%;
          left: 50%;
          transform: translate(-50%, -50%);
          width: 25px;
          height: 25px;
        }
      }
    }
  }
}

@media all and (max-width: '912px') {
  .team-wrapper {
    width: 135px;
    margin: 1rem 0;
    .img-container {
      height: 64px;
      width: 64px;
    }

    .member-contact {
      .member-title {
        font-size: 1rem;
        text-align: center;
      }
      .contact-links {
        .contact {
          margin: 0 0.5rem;
        }
      }
    }
  }
}
</style>
