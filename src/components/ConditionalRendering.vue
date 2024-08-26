<template>
  <h2 v-if="num === 0">The number is zero</h2>
  <h2 v-else-if="num < 0">The number is negative</h2>
  <h2 v-else-if="num > 0">The number is positive</h2>
  <h2 v-else>Not a number</h2>

  <template v-if="display">
    <h2>Victor</h2>
    <h2>Chandra</h2>
    <h2>Full Stack Engineer</h2>
  </template>

  <h2 v-show="showElement">Using v-show</h2>
  <h2 v-if="showElement">Using v-if</h2>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      num: 0,
      display: true,
      showElement: false
    }
  }
}
</script>

<style>

</style>