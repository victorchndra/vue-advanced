
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
  <!-- <watcher /> -->

  <!-- Component Props -->
  <component-props name="Victor" heroName="Spiderman" />
  <component-props name="Chandra" heroName="Superman" />
  <component-props :name="name" :heroName="channel" />
</template>

<script>
import BasicVueBinding from './components/BasicVueBinding.vue';
import BonusDirectives from './components/BonusDirectives.vue';
import ComponentProps from './components/ComponentProps.vue';
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
    Watcher,
    ComponentProps
  },
  data() {
    return {
      name: 'Vishwas',
      channel: 'Codevolution'
    }
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
