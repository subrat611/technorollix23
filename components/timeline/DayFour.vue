<template>
  <div class="outer">
    <div class="card">
      <div class="info">
        <h3 class="title">Battle of Bands (Finale)</h3>
        <div class="info-img">
          <nuxt-img src="/event/battleofband.png" />
        </div>
        <p>Time: 11:30 AM</p>
        <p>Venue: OAT</p>
      </div>
    </div>
    <div class="card">
      <div class="info">
        <h3 class="title">Valedictory & Prize Distribution</h3>
        <p>Time: 6:30 PM</p>
        <p>Venue: OAT</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DayThree',
}
</script>

<style lang="scss" scoped>
.outer {
  padding: 0 1rem;
  overflow: hidden;
}

/* Card container */
.card {
  position: relative;
  width: 800px;

  @media all and (max-width: '912px') {
    width: 300px;
  }
}

/* setting padding based on even or odd */
.card:nth-child(odd) {
  padding: 30px 0 30px 30px;
}
.card:nth-child(even) {
  padding: 30px 30px 30px 0;
}
/* Global ::before */
.card::before {
  content: '';
  position: absolute;
  width: 50%;
  border: solid orangered;
}

/* Setting the border of top, bottom, left */
.card:nth-child(odd)::before {
  left: 0px;
  top: -4.5px;
  bottom: -4.5px;
  border-width: 5px 0 5px 5px;
  border-radius: 50px 0 0 50px;
}

/* Setting the border of top, bottom, right */
.card:nth-child(even)::before {
  right: 0;
  top: 0;
  bottom: 0;
  border-width: 5px 5px 5px 0;
  border-radius: 0 50px 50px 0;
}

/* Removing the border if it is the first card */
.card:first-child::before {
  border-top: 0;
  border-top-left-radius: 0;
}

/* Removing the border if it is the last card  and it's odd */
.card:last-child:nth-child(odd)::before {
  border-bottom: 0;
  border-bottom-left-radius: 0;
}

/* Removing the border if it is the last card  and it's even */
.card:last-child:nth-child(even)::before {
  border-bottom: 0;
  border-bottom-right-radius: 0;
}

/* Information about the timeline */

.card {
  .info {
    display: flex;
    flex-direction: column;
    color: rgb(206, 206, 206);
    border-radius: 10px;
    padding: 10px;

    .title {
      font-size: 1.5rem;
      color: #fff;
      font-family: 'Poppins', sans-serif;
      letter-spacing: 0.04em;
      font-weight: 600;
      text-shadow: rgb(10 50 61 / 52%) 0px 0px 15px,
        rgb(91 213 247 / 62%) 0px 0px 15px,
        rgba(91, 213, 247, 0.507) 0px 0px 15px;
      position: relative;

      @media all and (max-width: '912px') {
        font-size: 1.2rem;
      }
    }

    p {
      color: rgba(255, 255, 255, 0.897);
      font-size: 1.1rem;
      font-family: 'Montserrat', sans-serif;
      font-weight: 500;
      letter-spacing: 0.05em;
      padding: 0.3rem 0;
    }

    .info-img {
      margin: 1rem 0;
      height: 100%;
      width: 300px;

      img {
        border-radius: 6px;
        height: 120px;
        width: 100%;
      }
    }
  }

  &:nth-child(even) {
    .info {
      display: flex;
      flex-direction: column;
      align-items: flex-end;
    }
  }
}

/* image of the card */

/* Title of the card */

/* Timeline dot  */
.title::before {
  content: '';
  position: absolute;
  width: 10px;
  height: 10px;
  background: white;
  border-radius: 999px;
  border: 3px solid orangered;
}

/* text right if the card is even  */
.card:nth-child(even) > .info > .title {
  text-align: right;
}

/* setting dot to the left if the card is odd */
.card:nth-child(odd) > .info > .title::before {
  left: -45px;
}

/* setting dot to the right if the card is odd */
.card:nth-child(even) > .info > .title::before {
  right: -45px;
}
</style>
