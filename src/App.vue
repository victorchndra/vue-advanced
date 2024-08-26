
<template>
  <!-- Basic Vue Binding -->
  <!-- <basic-vue-binding /> -->

  <!-- Conditional Rendering -->
  <!-- <conditional-rendering /> -->

  <!-- List Rendering -->
  <!-- <list-rendering /> -->

  <!-- Methods -->
  <!-- <methods /> -->

  <!-- Event Handling -->
  <!-- <event-handling /> -->
  
  <!-- Form Handling -->
  <!-- <form-handling /> -->

  <!-- Bonus Directives -->
  <!-- <bonus-directives /> -->

  <!-- Computed Properties -->
  <!-- <computed-properties /> -->

  <!-- Watcher -->
  <watcher />
</template>

<script>
import BasicVueBinding from './components/BasicVueBinding.vue';
import BonusDirectives from './components/BonusDirectives.vue';
import ComputedProperties from './components/ComputedProperties.vue';
import ConditionalRendering from './components/ConditionalRendering.vue';
import EventHandling from './components/EventHandling.vue';
import FormHandling from './components/FormHandling.vue';
import ListRendering from './components/ListRendering.vue';
import Methods from './components/Methods.vue';
import Watcher from './components/Watcher.vue';

export default {
  name: 'App',
  components: {
    FormHandling,
    BonusDirectives,
    BasicVueBinding,
    ConditionalRendering,
    ListRendering,
    Methods,
    EventHandling,
    BonusDirectives,
    ComputedProperties,
    Watcher
  },
  data() {
    return {}
  },
  methods: {}
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
