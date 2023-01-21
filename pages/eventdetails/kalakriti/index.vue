<template>
  <div class="event-details-wrapper">
    <back-btn />
    <div class="main-wrapper">
      <div class="details-wrapper">
        <p>
          Craft is the vehicle for expressing your vision. Craft is the visible
          edge of Art. Here we are with " Kalakriti " which is a unique Event
          driven by our artists' ideas, the context of space, season and the
          vibes of the region, you will Perceive - " Fiction turning into
          Reality". You are going to witness a different field of abstract
          painting, fine arts photography sculpture and many more....
        </p>
      </div>
      <div class="card-wrapper">
        <div
          v-for="({ param, eventName, eventDesc, img }, i) in events"
          :key="i"
          class="card-container"
        >
          <div class="card-img"><nuxt-img :src="'/event/' + img" /></div>
          <div class="card-content">
            <p class="card-title">{{ eventName.toUpperCase() }}</p>
            <p class="card-desc">
              {{ eventDesc }}
              <nuxt-link :to="`/eventdetails/kalakriti/` + param"
                >...more</nuxt-link
              >
            </p>
            <nuxt-link :to="`/eventdetails/kalakriti/` + param">
              <button>register</button>
            </nuxt-link>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'KalakritiEventCard',
  data() {
    return {
      events: [
        {
          param: 'exhibition',
          eventName: 'Pradarshini (Exhibition)',
          img: 'pradarshini.jpg',
          eventDesc:
            "Imagine what life would have been without colors, art and aesthetics boring right? And what Techno would be without an Art exhibition indeed boring. But don't worry",
        },
        {
          param: 'decoration',
          eventName: 'Drishyaam (Decoration)',
          img: 'drishyaam.jpg',
          eventDesc:
            'India is, the cradle of the human race, the birthplace of human speech, the mother of history, the grandmother of legend, and the great grandmother of tradition.',
        },
        {
          param: 'photorollix',
          eventName: 'Photorollix',
          img: 'photorollix.jpg',
          eventDesc:
            'Photorollix is a recreational event where in participants are welcomed to openly participate here to show their " third eye handling Skill " as it is said, The picture that you took with your camera',
        },
        {
          param: 'bestoutofwaste',
          eventName: 'Best out of Waste',
          img: 'bestoutofwaste.jpg',
          eventDesc:
            'It is a holistic event where Creative and attractive DIYs items are to be made from the recycled & Up cycled Stuffs which will worth in using as decor and they are Environment friendly.',
        },
        {
          param: 'rangoli',
          eventName: 'Rangoli',
          img: 'rangoli.jpg',
          eventDesc:
            'Rangoli is a very popular folk art that has several connotations across India. It is a spiritual distribution of colors Which represents the happiness, positivity and liveliness of a household',
        },
        {
          param: 'colourpainting',
          eventName: 'Colour Painting',
          img: 'colorpainting.jpg',
          eventDesc:
            'In order to create, we draw from our inner well. This inner well, an artistic reservoir, is ideally like a well-stocked fish pond… If we don’t give some attention to upkeep, our well is',
        },
        {
          param: 'glasspainting',
          eventName: 'Glass Painting',
          img: 'glasspainting.jpg',
          eventDesc:
            'Glass Painting Traditions of India is one of the most refined art forms, which emerged in the state of Gujarat in the beginning of the 18th century. Glass paintings are executed with',
        },
      ],
    }
  },
}
</script>

<style lang="scss" scoped>
a {
  color: #e5e5e5;
}

.event-details-wrapper {
  background: #000;
  color: #fff;
  min-height: 100vh;
  max-height: 100%;
  background-image: linear-gradient(to bottom, #00388b4f, #6b08663b);
  display: flex;
  justify-content: center;

  .main-wrapper {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 80%;

    .card-wrapper {
      width: 100%;
      margin: 2rem auto;
      display: flex;
      flex-wrap: wrap;
      justify-content: space-around;

      .card-container {
        margin: 1rem 0;
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
            text-transform: capitalize;
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
    }

    .details-wrapper {
      width: 95%;
      padding: 1rem;
      margin-top: 3rem;
      background: rgba(63, 194, 255, 0.11);
      border-radius: 7px;
      box-shadow: 0 4px 30px rgba(104, 104, 104, 0.1);
      backdrop-filter: blur(3.3px);
      -webkit-backdrop-filter: blur(3.3px);
      border: 1px solid rgba(255, 217, 252, 0.2);

      p {
        font-family: 'Roboto', sans-serif;
        font-size: 1.1rem;
        line-height: 1.6rem;
      }

      ul > li {
        padding: 0.3rem 0;
        margin-left: 1rem;
        font-size: 1.1rem;
        font-family: 'Roboto', sans-serif;
        line-height: 1.6rem;
      }
    }
  }
}

@media all and (max-width: '1156px') {
  .event-details-wrapper {
    .main-wrapper {
      width: 100%;
      .card-wrapper {
        width: 100%;
        margin: 2rem 0 3rem 0;
        padding: 0 1rem;

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

      .details-wrapper {
        margin-top: 6rem;
      }
    }
  }
}
</style>
