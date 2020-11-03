<template>
  <div :style="{ ...containerStyles }">
    <span :style="{ ...textStyles }" class="disableHiglight">
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
      required: true,
    },
    bgColor: {
      type: String,
      default: '#4285F4',
    },
    size: {
      type: String,
      default: '40',
    },
    textColor: {
      type: String,
      default: '#fff',
    },
    fontSize: {
      type: String,
      default: '18',
    },
  },
  computed: {
    containerStyles() {
      return {
        display: 'inline-flex',
        alignItems: 'center',
        justifyContent: 'center',
        background: this.bgColor,
        objectFit: 'cover',
        width: `${this.size}px`,
        height: `${this.size}px`,
        borderRadius: '50%',
      };
    },
    textStyles() {
      return {
        color: `${this.textColor}`,
        fontSize: `${this.fontSize}px`,
      };
    },
    getInitials() {
      const words = this.value.trim().split(/\s+/);
      return words.map((word) => word.charAt(0).toUpperCase());
    },
    initials() {
      return this.getInitials.join('');
    },
  },
};
</script>

<style scoped>
.disableHighlight {
  -webkit-touch-callout: none; /* iOS Safari */
  -webkit-user-select: none; /* Safari */
  -khtml-user-select: none; /* Konqueror HTML */
  -moz-user-select: none; /* Old versions of Firefox */
  -ms-user-select: none; /* Internet Explorer/Edge */
  user-select: none; /* Non-prefixed version, currently supported by Chrome, Edge, Opera and Firefox */
}
</style>
