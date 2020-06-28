<template>
  <div class="media-player-controls">
    <div></div>
    <div class="main-controls">
      <button class="media-pause"></button>
      <button class="media-next"></button>
    </div>
    <media-player-volume-control />
  </div>
</template>

<script>
import MediaPlayerVolumeControl from './MediaPlayerVolumeControl'

export default {
  components: {
    MediaPlayerVolumeControl
  }
}
</script>

<style lang="scss" scoped>
.main-controls {
  text-align: center;
}
.media-player-controls {
  display: flex;
  justify-content: space-between;
}
</style>
