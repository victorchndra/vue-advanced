<!-- #Basic Vue Binding -->
<!-- <script>
export default {
  name : "App",
  data() {
    return {
      headingId: "heading",
      isDisabled: true,
      status: "danger",
      isPromoted: false,
      isSoldout: true,
      highlightColor: 'orange',
      headerSize: 50,
      headerStyleObject: {
        color: 'orange',
        fontSize: '50px',
        padding: '20px'
      },
      baseStyleObject: {
        fontSize: '50px',
        padding: '10px'
      },
      successStyleObject: {
        color: 'green',
        backgroundColor: 'lightgreen',
        border: '1px solid green'
      },
      dangerStyleObject: {
        color: 'darked',
        backgroundColor: 'red',
        border: '1px solid darkred'
      }
    }
  }
}
</script> -->
<!-- <template>
  <h2 :id="headingId">Heading</h2>
  <button :disabled="isDisabled">Bind</button>
  <h2 class="underline">Underlined Text</h2>
  <h2 class="underline" :class="status">Status</h2>
  <h2 :class="isPromoted && 'promoted'">Promoted Movie</h2>
  <h2 :class="isSoldout ? 'sold-out' : 'new'">Soldout? Movie</h2>
  <h2 :class="['new', 'promoted']">Newly promoted movie</h2>
  <h2 :class="[isPromoted && 'promoted', isSoldout ? 'sold-out' : 'new']">Array Conditional movie</h2>
  <h2 :class="{
    promoted: isPromoted,
    new: !isSoldout,
    'sold-out': isSoldout
  }">Object Conditional Movie</h2>

  <h2 :style="{
    color: highlightColor,
    fontSize: headerSize + 'px',
    padding: '20px'
  }">Inline Style</h2>

  <h2 :style="headerStyleObject">Style Object</h2>

  <h2 :style="[baseStyleObject, successStyleObject]">Success Style</h2>
  <h2 :style="[baseStyleObject, dangerStyleObject]">Danger Style</h2>
</template> -->

<!-- Conditional Rendering -->
<!-- <script>
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
</script> -->
<!-- <template>
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

</template> -->

<!-- List Rendering -->
<!-- <script>
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
</script> -->
<!-- <template>
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
</template> -->

<!-- Methods -->
<template>
  <h2>{{ 2 + 3 + 5 }}</h2>
  <h2>Add method - {{ add(10, 15, 20) }}</h2>
</template>
<script>
  export default {
    name: 'App',
    data() {
      return {

      }
    },
    methods: {
      add(a, b, c) {
        return a + b + c
      }
    }
  }
</script>

<style scoped>
.underline {
  text-decoration: underline;
}

.promoted {
  font-style: italic;
}

.new {
  color: olivedrab;
}

.sold-out {
  color: red;
}
</style>
