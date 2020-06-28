<template>
  <div class="jb-avatar">
    <img
      :src="avatar"
      :style="{
        width: size,
        height: size
      }"
    />
  </div>
</template>

<script>
export default {
  name: 'JbAvatar',
  props: {
    avatar: {
      type: String,
      default: require('~/assets/images/avatar.jpg')
    },
    size: {
      type: String,
      default: '40px'
    }
  }
}
</script>

<style lang="scss" scoped>
.jb-avatar > img {
  object-fit: cover;
  border-radius: 100%;
}
</style>
