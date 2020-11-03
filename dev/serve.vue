<script>
import Vue from 'vue';
import VueInitialsPlaceholder from '@/vue-initials-placeholder.vue';

export default Vue.extend({
  name: 'ServeDev',
  components: {
    VueInitialsPlaceholder
  }
});
</script>

<template>
  <div id="app">
    <vue-initials-placeholder />
  </div>
</template>
