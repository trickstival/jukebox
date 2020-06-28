<template>
  <div class="media-player">
    <iframe
      ref="iframe"
      :height="videoHeight"
      src="https://www.youtube.com/embed/1rziSlOiIPk"
      frameborder="0"
      allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
      class="yt-iframe"
      allowfullscreen
    ></iframe>
    <media-player-controls />
  </div>
</template>

<script>
import MediaPlayerControls from './MediaPlayerControls'

export default {
  components: {
    MediaPlayerControls
  },
  data() {
    return {
      videoHeight: 0
    }
  },
  mounted() {
    window.addEventListener('resize', this.updateVideoHeight)
    this.updateVideoHeight()
  },
  beforeDestroy() {
    console.log('destroying')
    window.removeEventListener('resize', this.updateVideoHeight)
  },
  methods: {
    updateVideoHeight() {
      console.log('resizing')
      this.videoHeight = this.$refs.iframe.clientWidth / (16 / 9)
    }
  }
}
</script>

<style lang="scss" scoped>
.media-player {
}
.yt-iframe {
  width: 100%;
}
</style>
