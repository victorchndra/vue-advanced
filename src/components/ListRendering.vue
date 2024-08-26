<template>
  <template v-for="name in names" :key="name">
    <h2 v-if="name === 'Victor'">{{ name }}</h2>
  </template>
  <h2 v-for="(name, index) in names" :key="index">{{ index }} {{ name }}</h2>
  <h2 v-for="(name, index) in fullNames" :key="index">{{ name.first }} {{ name.last }}</h2>
  <div v-for="(actor, index) in actors" :key="index">
    <h2>{{ actor.name }}</h2>
    <h3 v-for="movie, index in actor.movies" :key="index">{{ movie }}</h3>
  </div>
  <h2 v-for="value, key, index in myInfo" :key="index">{{ key }}: {{ value }}</h2>
  <template v-for="value in myInfo" :key="value">
    <h2>{{ value }}</h2>
    <hr />
  </template>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      names: ['Victor', 'Chandra', 'Andi', 'Budi'],
      fullNames: [
        { first: 'Bruce', last: 'Wayne' },
        { first: 'Clark', last: 'Kent' },
        { first: 'Princess', last: 'Diana' },
      ],
      actors: [
        {
          name: 'Christian Bale',
          movies: ['Batman', 'The Prestige']
        },
        {
          name: 'Di Caprio',
          movies: ['Titanic', 'Inception']
        },
      ],
      myInfo: {
        name: 'Vishwas',
        channel: 'Codevolution',
        course: 'Vue 3'
      }
    }
  }
}
</script>

<style>

</style>