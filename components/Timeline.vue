<template>
  <div class="timeline">
    <div class="timeline__item">
      <div class="timeline__label">{{ label }}</div>
      <div class="timeline__body">
        <div class="timeline__title">{{ title }}</div>
        <div class="timeline__image"></div>
        <div class="timeline__subtitle">{{ subtitle }}</div>
        <div class="timeline__description">{{ description }}</div>
      </div>
    </div>
    <div class="timeline__item">
      <div class="timeline__label">{{ label }}</div>
      <div class="timeline__body">
        <div class="timeline__title">{{ title }}</div>
        <div class="timeline__image"></div>
        <div class="timeline__subtitle">{{ subtitle }}</div>
        <div class="timeline__description">{{ description }}</div>
      </div>
    </div>
    <div class="timeline__item">
      <div class="timeline__label">{{ label }}</div>
      <div class="timeline__body">
        <div class="timeline__title">{{ title }}</div>
        <div class="timeline__image"></div>
        <div class="timeline__subtitle">{{ subtitle }}</div>
        <div class="timeline__description">{{ description }}</div>
      </div>
    </div>
    <div class="timeline__item">
      <div class="timeline__label">{{ label }}</div>
      <div class="timeline__body">
        <div class="timeline__title">{{ title }}</div>
        <div class="timeline__image"></div>
        <div class="timeline__subtitle">{{ subtitle }}</div>
        <div class="timeline__description">{{ description }}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    label: String,
    title: String,
    subtitle: String,
    description: String
  }
}
</script>

<style lang="scss" scoped>
.timeline {
  position: relative;
  margin: 40px 0;
  color: black;

  &__item {
    position: relative;
    margin-top: 24px;
  }

  &__label {
    position: absolute;
    top: -16px;
    left: 40px;
    width: fit-content;
    padding: 6px;
    background: rgba(255,255,255,0.5);
    backdrop-filter: blur(30px);
    box-shadow: 0 0 4px 0 rgba(255, 255, 255, 0.4);
    border-radius: 4px;
    border-bottom-right-radius: 0;
    border-top-right-radius: 0;

    &::before {
      content: "";
      top: 0;
      left: 100%;
      width: 0;
      height: 0;
      position: absolute;
      border-top: 17px solid transparent !important;
      border-bottom: 16px solid transparent !important;
      border-right: 10px solid transparent !important;
      border-left: 10px solid transparent;
      border-color: rgba(255,255,255,0.4);
    }
  }

  &__body {
    margin-left: 200px;

    &::before {
      content: "";
      position: absolute;
      width: 6px;
      height: 6px;
      background: black;
      border-radius: 50%;
      top: 0;
      left: 178px;
    }
  }

  &::before {
    content: "";
    position: absolute;
    width: 2px;
    top: 0;
    height: 100%;
    background: black;
    left: 180px;
  }

  &__title {
    font-size: 20px;
    font-weight: 400;
    color: white;
  }

  &__subtitle {
    font-size: 16px;
    font-weight: 300;
    color: white;
  }

  &__description {
    font-size: 12px;
    font-weight: 300;
    color: white;
    margin: 6px 0;
  }
}
</style>
