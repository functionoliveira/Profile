<template>
  <div class="background-video">
    <button class="background-video__audio" @click="handleBtnAudioClick">Ouvir</button>
    <video :src="srcVideo" loop autoplay :muted="muted"></video>
  </div>
</template>

<script>
export default {
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
  z-index: -1;

  video {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  &__audio {
    position: absolute;
    top: 20px;
    left: 20px;
    z-index: 999;
  }
}
</style>
