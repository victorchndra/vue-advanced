<template>
  <h2>Volume Tracker (0-20)</h2>
  <h3>Current Volume - {{ volume }}</h3>
  <div>
    <button @click="volume += 2">Increase</button>
    <button @click="volume -= 2">Decrease</button>
  </div>
  <input type="text" v-model="movie">
  <input type="text" v-model="movieInfo.title">
  <input type="text" v-model="movieInfo.actor">
  <div>
    <button @click="movieList.push('Wonder Woman')">Add Movie</button>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      volume: 0,
      movie: 'Batman',
      movieInfo: {
        title: '',
        actor: ''
      },
      movieList: ['Batman', 'Superman']
    }
  },
  methods: {},
  computed: {},
  watch: {
    volume(newValue, oldValue) { //volume is got from data property
      if(newValue > oldValue && newValue === 16) {
        alert('Listening to a high volume for a long time may damage your hearing')
      }
    },
    movie: {
      handler(newValue) {
        console.log(`Calling API with movie name = ${newValue}`)
      },
      immediate: true
    },
    movieInfo: {
      handler(newValue) {
        console.log(`Calling API with movie title = ${newValue.title} and actor = ${newValue.actor}`);
      },
      deep: true
    },
    movieList: {
      handler(newValue) {
        console.log(`Updated list ${newValue}`)
      },
      deep: true
    }
  }
}
</script>

<style>

</style>