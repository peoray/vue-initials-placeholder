<template>
  <div>
    <span>
      {{ initials }}
    </span>
  </div>
</template>

<script>
export default {
  name: 'vue-initials-placeholder',
  props: {
    value: {
      type: String,
      required: true
    },
  },
  computed: {
    getInitials() {
      const words = this.value.trim().split(/\s+/)
      return words.map((word) => word.charAt(0).toUpperCase())
    },
    initials() {
      return this.getInitials.join('')
    }
  }
};
</script>

<style scoped></style>
