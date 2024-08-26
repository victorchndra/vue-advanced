<template>
  <h2>{{ name }}</h2>
  <div>
    <button v-on:click="changeName($event), increment(1, $event)">Change name</button>
  </div>

  <h2>{{ count }}</h2>
  <div>
    <button @click="increment(2, $event)">Increment</button>
    <button @click="decrement(1)">Decrement</button>
  </div>
</template>

<script>
export default {
    name: 'App',
    data() {
      return {
        name: 'Victor',
        count: 0
      }
    },
    methods: {
      changeName(event) {
        this.name = 'Batman'
        console.log('Event', event)
      },
      increment(num, event) {
        this.count += num
        console.log('Event', event)
      },
      decrement(num) {
        this.count -= num
      }
    }
  }
</script>

<style>

</style>