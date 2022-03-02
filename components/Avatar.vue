<template>
  <div class="avatar">
    <img :src="image" :alt="description">
  </div>
</template>

<script>
export default {
  props: {
    image: String,
    description: String
  }
}
</script>

<style lang="scss" scoped>
.avatar {
    width: 80px;
    height: 80px;
    border-radius: 50%;
    overflow: hidden;
    border: 4px solid white;

    img {
        width: 100%;
        height: 100%;
        object-fit: cover;
    }
}
</style>
