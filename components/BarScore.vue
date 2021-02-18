<template>
  <div class="bar-score">
    <div class="bar-score__header">
      <slot></slot>
      <div class="bar-score__title">{{ title }}</div>
      <span class="bar-score__label">{{ score + '%' }}</span>
    </div>
    <div class="bar-score__wrap">
      <div class="score"></div>
      <div class="value" :style="{ width: score + '%' }"></div>
    </div>
    <small>{{ legend }}</small>
  </div>
</template>
<script>
export default {
  props: {
    title: String,
    score: Number,
    legend: String
  }
}
</script>
<style lang="scss" scoped>
.bar-score {
  margin-bottom: 12px;
  
  &__header {
    display: flex;
  }

  &__wrap {
    position: relative;
    width: 100%;
    height: 6px;
    border: 1px solid white;
    border-radius: 3px;
  }

  &__title {
    flex: 1 1 0;
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

  .score {
    width: 100%;
    height: 5px;
    position: relative;
    background: rgba(255, 255, 255, 0.3);
    box-shadow: 0 0 3px 0 rgba(255, 255, 255, 0.5);
  }

  .value {
    width: 50%;
    height: 5px;
    top: 0;
    position: absolute;
    background: $main-color;
    z-index: -1;
  }

  small {
    font-weight: 300;
    letter-spacing: 1px;
    color: white;
  }

  svg {
    width: 20px;
    height: 20px;
    margin-right: 6px;
  }
}
</style>
