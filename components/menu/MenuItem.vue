<template>
  <a class="menu-item" :href="anchor">
    <div class="menu-item__icon">
      <svg viewBox="0 0 24 24">
        <path fill="currentColor" d="M10,20V14H14V20H19V12H22L12,3L2,12H5V20H10Z" />
      </svg>
    </div>
    <div class="menu-item__label">{{ label }}</div>
  </a>
</template>

<script>
export default {
  props: {
    label: String,
    anchor: String
  }
}
</script>

<style lang="scss" scoped>
.menu-item {
  padding: 4px;
  margin: 4px 0;
  display: flex;
  align-items: center;
  text-decoration: none;
  cursor: pointer;

  &__icon {
    width: 24px;
    height: 24px;
    margin-right: 4px;
    color: white;
  }

  &__label {
    font-weight: 600;
  }
}
</style>
