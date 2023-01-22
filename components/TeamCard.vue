<template>
  <div>
    <div class="team-card">
      <nuxt-img :src="'/team/' + member.image" format="webp" loading="lazy" />
      <div class="overlay">
        <p class="title">{{ member.name }}</p>
        <p class="desig">{{ member.designation }}</p>
      </div>
      <div class="overlay-hover">
        <div class="contact-links">
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
          <div class="contact">
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
        </div>
      </div>
    </div>
    <div class="contact-container-mobile">
      <div class="contact-links">
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
        <div class="contact">
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
      </div>
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
.contact-container-mobile {
  display: none;
  padding: 1rem 0;

  .contact-links {
    height: 100%;
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

.team-card {
  width: 250px;
  height: 250px;
  border-radius: 3px;
  margin: 2rem 1rem 1rem 1rem;
  // background: #edf2f4;
  position: relative;
  // background: #000;
  // background-image: radial-gradient(
  //   circle farthest-corner at 1.1% 2.5%,
  //   rgba(0, 113, 208, 1) 0%,
  //   rgba(0, 160, 247, 1) 24%,
  //   rgb(140, 2, 175) 71.9%
  // );

  img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: top;
    transition: transform 200ms cubic-bezier(0.68, -0.55, 0.27, 1.55);
  }

  .overlay-hover {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    opacity: 0;
    background: linear-gradient(to bottom, #63084900, #0e0e558c);
    border-bottom: 3px solid #fff;
    transition: opacity 500ms ease-in-out;

    .contact-links {
      height: 100%;
      display: flex;
      justify-content: space-evenly;
      align-items: flex-end;
      padding-bottom: 1.2rem;

      .contact {
        height: 35px;
        width: 35px;
        background: #fff;
        border-radius: 12px;
        padding: 1rem;
        position: relative;

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

  .overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    // background: rgba(7, 7, 7, 0.5);
    background-image: linear-gradient(to bottom, #63084900, #0909467e);
    // background-image: linear-gradient(
    //   178.8deg,
    //   rgba(0, 88, 143, 0.233) 13.8%,
    //   rgba(21, 189, 240, 0.103) 95.4%
    // );
    color: #fff;
    padding: 2rem 0.5rem;
    transition: all 300ms ease-in-out;

    .title {
      position: absolute;
      bottom: 13%;
      color: #ffffff;
      font-family: 'Montserrat', sans-serif;
      font-weight: bolder;
      letter-spacing: 0.05em;
      font-size: 1.1rem;
      margin-bottom: 0.2rem;
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
      font-size: 0.9rem;
      text-shadow: rgb(241, 241, 241) 0px 0px 1px,
        rgba(216, 216, 216, 0.568) 0px 0px 2px;
    }
  }

  &:hover {
    overflow: hidden;

    img {
      transform: scale(1.02);
    }

    .overlay-hover {
      opacity: 1;
    }
    .overlay {
      opacity: 0;
    }
  }
}

@media all and (max-width: '1200px') {
  .contact-container-mobile {
    display: block;
  }

  .team-card {
    margin: 1rem;
    &:hover {
      .overlay-hover {
        display: none;
      }
      .overlay {
        opacity: 1;
      }
    }
  }
}

@media all and (max-width: '912px') {
  .team-card {
    .overlay {
      .title {
        font-size: 1.1rem;
        margin-bottom: 0.2rem;
      }
      .desig {
        font-size: 0.8rem;
      }
    }
  }
}
</style>
