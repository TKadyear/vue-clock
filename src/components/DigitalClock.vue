<script>

export default {
  name: "DigitalClock",
  data() {
    return {
      hours: 0,
      minutes: 0,
      seconds: 0
    }
  },
  mounted() {
    setInterval(() => this.setTime(), 1000)
  },
  methods: {
    setTime() {
      const date = new Date();
      this.hours = date.getHours();
      this.minutes = date.getMinutes();
      this.seconds = date.getSeconds();
    }
  }
}
</script>

<template>
  <h1>Digital Clock</h1>
  <div class="container">
    <div class="LCD">
      <div class="hours">{{ hours }}</div>
      <div class="divider">:</div>
      <div class="minutes">{{ minutes }}</div>
      <div class="divider">:</div>
      <div class="seconds">{{ seconds }}</div>
    </div>
  </div>
</template>

<style scoped>
.LCD {
  display: flex;
}
</style>
