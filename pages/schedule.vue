<template>
  <div>
    <!-- navigation -->
    <nav-bar />
    <nav-bar-two />
    <div class="schedule-wrapper">
      <div class="schedule-selector-wrapper">
        <select @change="(e) => displayTimeLine(e)">
          <option value="1 march">1st March, 2023 (Wednesday)</option>
          <option value="2 march">2nd March, 2023 (Thursday)</option>
          <option value="3 march">3rd March, 2023 (Friday)</option>
          <option value="4 march">4th March 2023 (Saturday)</option>
        </select>
      </div>
      <div class="timeline">
        <day-one v-show="dayone" />
        <day-two v-show="daytwo" />
        <day-three v-show="daythree" />
        <day-four v-show="dayfour" />
      </div>
    </div>
    <nav-bar-three />
  </div>
</template>

<script>
import DayFour from '~/components/timeline/DayFour.vue'
import DayOne from '~/components/timeline/DayOne.vue'
import DayThree from '~/components/timeline/DayThree.vue'
import DayTwo from '~/components/timeline/DayTwo.vue'

export default {
  name: 'SchedulePage',
  components: { DayOne, DayTwo, DayThree, DayFour },
  data() {
    return {
      dayone: true,
      daytwo: false,
      daythree: false,
      dayfour: false,
      alldays: true,
    }
  },
  methods: {
    displayTimeLine(e) {
      if (e.target.value === '1 march') {
        this.dayone = true
        this.daytwo = false
        this.daythree = false
        this.dayfour = false
      }

      if (e.target.value === '2 march') {
        this.dayone = false
        this.daytwo = true
        this.daythree = false
        this.dayfour = false
      }

      if (e.target.value === '3 march') {
        this.dayone = false
        this.daytwo = false
        this.daythree = true
        this.dayfour = false
      }

      if (e.target.value === '4 march') {
        this.dayone = false
        this.daytwo = false
        this.daythree = false
        this.dayfour = true
      }
    },
  },
}
</script>

<style scoped lang="scss">
.schedule-wrapper {
  min-height: 100vh;
  max-height: 100%;
  background: #111;
  padding: 1rem 0;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  .schedule-selector-wrapper {
    margin-top: calc(1.6rem + 7rem);

    @media all and (max-width: '912px') {
      & {
        margin-top: 2rem;
      }
    }

    select {
      outline: none;
      padding: 0.5rem 1rem;
      font-size: 1.2rem;
      border-radius: 3px;
      font-family: 'Montserrat', sans-serif;
      font-weight: 500;
      cursor: pointer;
      color: #fff;
      background: rgba(255, 255, 255, 0.116);
      box-shadow: 0 4px 30px rgba(255, 255, 255, 0.1);
      backdrop-filter: blur(3.3px);
      -webkit-backdrop-filter: blur(3.3px);

      option {
        background-color: #333;
        color: rgb(252, 101, 63);
      }
    }
  }
}

/* Timeline Container */
.timeline {
  margin: 7rem 0;
  width: 100%;
  display: flex;
  justify-content: center;
}
</style>
