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
<!-- <template>
  <h2>{{ 2 + 3 + 5 }}</h2>
  <h2>Add method - {{ add(10, 15, 20) }}</h2>
  <h2>Multiply method - {{ multiply(baseValue) }}</h2>
</template> -->
<!-- <script>
  export default {
    name: 'App',
    data() {
      return {
        baseMultiplier: 5,
        baseValue: 2
      }
    },
    methods: {
      add(a, b, c) {
        return a + b + c
      },
      multiply(num) {
        return num * this.baseMultiplier
      }
    }
  }
</script> -->

<!-- Event Handling -->
<!-- <template>
  <h2>{{ name }}</h2>
  <div>
    <button v-on:click="changeName($event), increment(1, $event)">Change name</button>
  </div>

  <h2>{{ count }}</h2>
  <div>
    <button @click="increment(2, $event)">Increment</button>
    <button @click="decrement(1)">Decrement</button>
  </div>
</template> -->
<!-- <script>
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
</script> -->

<!-- Form Handling -->
<template>
  <div>
    <pre>
      {{ JSON.stringify(formValues, null, 2) }}
    </pre>
  </div>
  <form @submit="submitForm">
    <!-- input -->
    <div>
      <label for="name">Name</label>
      <input type="text" id="name" v-model.trim="formValues.name">
    </div>

    <!-- text area input -->
    <div>
      <label for="profile">Profile Summary</label>
      <textarea id="profile" v-model="formValues.profileSummary"></textarea>
    </div>

    <!-- single select -->
    <div>
      <label for="country">Country</label>
      <select id="country" v-model="formValues.country">
        <option value="">Select a country</option>
        <option value="india">India</option>
        <option value="vietnam">Vietnam</option>
        <option value="singapore">Singapore</option>
      </select>
    </div>

    <!-- multiple select -->
    <div>
      <label for="job-location">Job Location</label>
      <select id="job-location" multiple v-model="formValues.jobLocation">
        <option value="india">India</option>
        <option value="vietnam">Vietnam</option>
        <option value="singapore">Singapore</option>
      </select>
    </div>

    <!-- single checkbox -->
    <div>
      <input type="checkbox" id="remoteWork" v-model="formValues.remoteWork" true-value="yes" false-value="no">
      <label for="remoteWork">Open to remote work?</label>
    </div>

    <!-- multiple checkbox -->
    <div>
      <label>Skill Set</label>
      <input type="checkbox" id="html" value="html" v-model="formValues.skillSet">
      <label for="html">HTML</label>
      <input type="checkbox" id="css" value="css" v-model="formValues.skillSet">
      <label for="css">CSS</label>
      <input type="checkbox" id="javascript" value="javascript" v-model="formValues.skillSet">
      <label for="javascript">JavaScript</label>
    </div>

    <!-- radio group -->
    <div>
      <label>Years of Experience</label>
      <input type="radio" id="0-2" value="0-2" v-model="formValues.yearsOfExperience">
      <label for="0-2">0-2</label>
      <input type="radio" id="3-5" value="3-5" v-model="formValues.yearsOfExperience">
      <label for="3-5">3-5</label>
      <input type="radio" id="6-10" value="6-10" v-model="formValues.yearsOfExperience">
      <label for="6-10">6-10</label>
      <input type="radio" id="10+" value="10+" v-model="formValues.yearsOfExperience">
      <label for="10+">10+</label>
    </div>

    <!-- submit -->
    <div>
      <button>Submit</button>
    </div>
  </form>
</template>
<script>
export default {
  name: 'App',
  data() {
    return {
      formValues: {
        name: '',
        profileSummary: '',
        country: '',
        jobLocation: [],
        remoteWork: 'no',
        skillSet: [],
        yearsOfExperience: '',
        age: null,
      }
    }
  },
  methods: {
    submitForm(event) {
      event.preventDefault();
      console.log('Form values', this.formValues)
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
