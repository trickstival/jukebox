<template>
  <div class="app">
    <div class="main-page">
      <jb-header />
      <jb-media-experience class="jb-media-experience" />
    </div>
  </div>
</template>

<script>
import JbHeader from '~/components/common/JbHeader.vue'
import JbMediaExperience from '~/components/player/JbMediaExperience'

export default {
  components: {
    JbHeader,
    JbMediaExperience
  }
}
</script>

<style lang="scss" scoped>
.app,
.main-page {
  position: absolute;
  width: 100%;
  height: 100%;
}
.jb-media-experience {
  flex-grow: 1;
}
.main-page {
  display: flex;
  flex-direction: column;
}
</style>
