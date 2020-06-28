<template>
  <div class="media-experience-actions">
    <fab>Ac1</fab>
    <fab>Ac2</fab>
    <fab>Ac3</fab>
  </div>
</template>

<script>
import Fab from '~/components/common/Fab'

export default {
  components: {
    Fab
  }
}
</script>

<style lang="scss" scoped>
.media-experience-actions {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  column-gap: 20px;
}
</style>
