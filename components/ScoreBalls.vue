<template>
  <div class="score-balls">
    <div class="score-balls__title">{{ title }}</div>
    <div class="score-balls__wrap">
      <div class="ball" v-bind:class="{ fill: i < score }" v-for="i in balls" :key="i"></div>
      <span class="score-balls__label">{{ label }}</span>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    icon: String,
    title: String,
    label: String,
    score: Number
  },
  data () {
    return {
      balls: [0, 1, 2 , 3, 4, 5, 6, 7, 8, 9]
    }
  }
}
</script>
<style lang="scss" scoped>
.score-balls {
  margin-bottom: 12px;

  &__wrap {
    display: flex;
  }

  &__title {
    text-transform: capitalize;
    background: linear-gradient(180deg, white 10%, #7ac2d4 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    font-weight: 600;
    margin-bottom: 6px;
  }

  &__label {
    line-height: 20px;
  }

  .ball {
    position: relative;
    width: 20px;
    height: 20px;
    border-radius: 50%;
    border: 1px solid white;
    margin-right: 6px;
    background: rgba(white, .3);
    box-shadow: inset 0 0 5px 0 rgba(white, 0.5);
    overflow: hidden;

    &::before {
      top: -5px;
      left: -5px;
      position: absolute;
      width: 30px;
      height: 30px;
      content: "";
      z-index: -1;
    }

    &.fill {
      &::before {
        background: $main-color;
      }
    }
  }
}
</style>
