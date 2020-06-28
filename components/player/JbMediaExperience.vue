<template>
  <section class="media-experience">
    <div class="media-experience-content">
      <media-experience-header />
      <media-player class="media-player" />
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
.media-player {
  flex-grow: 1;
}
.media-experience-content {
  display: flex;
  flex-direction: column;
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
