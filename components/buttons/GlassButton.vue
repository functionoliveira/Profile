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
  border: 2px solid white;
  background: transparent;
  transition: 0.2s all ease-in-out;

  label { cursor: pointer; }

  &:hover {
    background: linear-gradient(230deg, rgba(35, 30, 210, 0.4) 0%, rgba(240, 20, 165, 0.4) 100%);
    backdrop-filter: blur(30px);
    border-color: transparent;
  }

  &:active {
    border-color: white;
  }
}
</style>
