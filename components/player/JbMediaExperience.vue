<template>
  <section class="media-experience">
    <div class="media-experience-content">
      <media-experience-header />
      <media-player />
    </div>
  </section>
</template>

<script>
import MediaPlayer from './MediaPlayer'
import MediaExperienceHeader from './MediaExperienceHeader'

export default {
  components: {
    MediaPlayer,
    MediaExperienceHeader
  }
}
</script>

<style lang="scss" scoped>
.media-experience-content {
  padding: 20px;
  width: 100%;
  max-width: 900px;
}
.media-experience {
  display: flex;
  justify-content: center;
  align-content: center;
}
</style>
