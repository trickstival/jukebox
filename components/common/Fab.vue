<template>
  <button
    :style="{
      backgroundColor: color,
      width: size,
      height: size
    }"
    class="fab"
  >
    <slot />
  </button>
</template>

<script>
export default {
  name: 'Fab',
  props: {
    size: {
      default: '40px',
      type: String
    },
    color: {
      default: '#ccc',
      type: String
    }
  }
}
</script>

<style lang="scss" scoped>
.fab {
  padding: 0;
  border-radius: 100%;
}
</style>
