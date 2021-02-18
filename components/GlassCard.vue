<template>
  <div class="glass-card">
    <slot></slot>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.glass-card {
    position: relative;
    padding: 12px;
    text-align: left;
    border-radius: 4px;
    background: $main-gradient;
    backdrop-filter: blur(30px);
    box-shadow: 0 0 10px 0 rgba(#000, 0.6);
    overflow: hidden;
}
</style>
