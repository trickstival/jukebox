<template>
  <header class="jb-media-experience-header">
    <div class="song-info">
      <jb-avatar />
      <div class="is-playing">
        <div>
          salomaosnff is playing
        </div>
        <h3 class="current-song-title">
          Jessé - Porto Solidão
        </h3>
      </div>
    </div>
    <media-experience-actions />
  </header>
</template>

<script>
import MediaExperienceActions from './MediaExperienceActions'
import JbAvatar from '~/components/common/JbAvatar'

export default {
  components: {
    JbAvatar,
    MediaExperienceActions
  }
}
</script>

<style lang="scss" scoped>
.song-info {
  display: flex;
  align-items: center;
}
.is-playing {
  margin-left: 15px;
}
.jb-media-experience-header {
  display: flex;
  justify-content: space-between;
  width: 100%;
}
</style>
