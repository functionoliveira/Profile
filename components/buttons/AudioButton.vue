<template>
  <button class="audio-button" @click="$emit('click')">
    <volume-on v-if="!muted" />
    <volume-off v-else />
  </button>
</template>

<script>
import VolumeOn from '~/icons/VolumeOn'
import VolumeOff from '~/icons/VolumeOff'
export default {
  components: { VolumeOn, VolumeOff },
  props: {
    muted: Boolean
  }
}
</script>

<style lang="scss" scoped>
.audio-button {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 60px;
  height: 60px;
  border-radius: 50%;
  padding: 8px;
  outline: none;
  cursor: pointer;
  background: linear-gradient(230deg, rgba(35, 30, 210, 0.4) 0%, rgba(240, 20, 165, 0.4) 100%);
  backdrop-filter: blur(30px);
  border-color: rgba(#fff, 0.25);
  box-shadow: 0 0 10px 0 rgba(#fff, 0.6);
  transition: 0.2s all ease-in-out;

  &:hover {
    backdrop-filter: blur(0);
    box-shadow: 0 0 0 0 rgba(#fff, 0.6);
    border: 2px solid rgba(#fff, 0.75);
    transition: none;
  }

  &:active {
    background: transparent;
  }

  svg, svg * {
    width: 32px;
    height: 32px;
    color: rgba(#fff, 0.25);
    fill: rgba(#fff, 0.25);
  }
}
</style>
