<template>
  <div id="app">
    <vue-initials-placeholder
      value="Emmanuel Raymond"
      size="80"
      fontSize="32"
    />
  </div>
</template>

<script>
import Vue from 'vue';
import VueInitialsPlaceholder from '@/vue-initials-placeholder.vue';

export default Vue.extend({
  name: 'ServeDev',
  components: {
    VueInitialsPlaceholder,
  },
});
</script>

<style scoped></style>
