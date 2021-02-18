<template>
  <div class="scroll" @mouseenter="over=true" @mouseleave="over=false" v-bind:class="[{ 'scroll-show' : over, 'close' : !open }]">
    <slot></slot>
  </div>
</template>

<script>
export default {
  data () {
    return {
      open: true,
      over: false
    }
  }
}
</script>

<style lang="scss" scoped>
.scroll {
  height: calc(100vh - 72px);
  overflow: auto;
  box-sizing: content-box;
  padding: 12px 12px 36px 12px;
  margin-top: -12px;
  color: rgba(0, 0, 0, 0);
  transition: color .3s ease;
  scroll-behavior: smooth;

  &::-webkit-scrollbar-thumb {
    border-radius: 5px;
    background: rgba(0,0,0,0);
    box-shadow: inset 0 0 0 5px;
  }

  &::-webkit-scrollbar,
  &::-webkit-scrollbar-thumb {
    width: 6px;
    border-radius: 3px;
    background-clip: padding-box;
    border: 0px solid transparent;
  }

  &.scroll-show {
    color: var(--clientTextColor);

    &::-webkit-scrollbar-track {
      -webkit-box-shadow: inset 0 0 6px rgba(0,0,0,0.3);
    }
  }
}
</style>
