<template>
  <button class="glass-button">
    <label>{{ label }}</label>
  </button>
</template>

<script>
export default {
  props: {
    label: String
  }
}
</script>

<style lang="scss" scoped>
.glass-button {
  padding: 14px;
  font-weight: 600;
  font-size: 16px;
  letter-spacing: 2px;
  outline: none;
  cursor: pointer;
  border-radius: 2px;
  background: linear-gradient(230deg, rgba(35, 30, 210, 0.4) 0%, rgba(240, 20, 165, 0.4) 100%);
  backdrop-filter: blur(30px);
  border-color: transparent;
  box-shadow: 0 0 10px 0 rgba(#fff, 0.6);

  label { cursor: pointer; }

  &:hover {
    backdrop-filter: blur(0);
    box-shadow: 0 0 0 0 rgba(#fff, 0.6);
    border: 2px solid white;
  }

  &:active {
    background: transparent;
  }
}
</style>
