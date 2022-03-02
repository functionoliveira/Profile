<template>
  <div class="background-video">
    <div  class="background-video__audio">
      <audio-button @click="handleBtnAudioClick" :muted="muted" />
    </div>
    <video :src="srcVideo" loop autoplay :muted="muted"></video>
  </div>
</template>

<script>
import AudioButton from '~/components/buttons/AudioButton'
export default {
  components: { AudioButton },
  props: {
    srcVideo: String
  },
  data () {
    return {
      muted: true
    }
  },
  methods: {
    handleBtnAudioClick () {
      this.muted = !this.muted;
    }
  }
}
</script>

<style lang="scss" scoped>
.background-video {
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  position: fixed;
  z-index: 0;

  video {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  &__audio {
    position: absolute;
    bottom: 36px;
    left: 36px;
    z-index: 999;
  }
}
</style>
