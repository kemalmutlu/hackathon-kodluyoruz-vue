<template>
  <div class="timer">
    <h1>Time left to the next Hackathon</h1>
    <h3>Machine Learning Hackathon</h3>
    <flip-countdown deadline="2020-12-30 22:22:22"></flip-countdown>
  </div>
</template>

<script>
import FlipCountdown from 'vue2-flip-countdown'
export default {
    components: { FlipCountdown }
}
</script>

<style scoped>
.timer {
  margin-top: 30px;
  text-align: center;
}
</style>