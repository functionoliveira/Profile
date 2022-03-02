<template>
  <div class="brief">
    <a href="www.linkedin.com" class="brief__link">
      <avatar />
    </a>
    <span class="brief__title">Nome Teste</span>
    <p class="brief__text">"Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque lectus augue, aliquet eget lorem non, dapibus accumsan tellus. Nunc auctor, purus ac mattis eleifend, nibh mauris auctor nisi, in elementum velit erat a elit. Donec eu ullamcorper justo."</p>
  </div>
</template>
<script>
import Avatar from '~/components/Avatar';
export default {
  components: { Avatar }
}
</script>

<style lang="scss" scoped>
.brief {
  display: flex;
  flex-flow: column;
  justify-content: center;
  align-items: center;
  width: 100%;

  &__link {
    width: 180px;
    height: 180px;
    margin-bottom: 10px;

    .avatar {
      width: 100%;
      height: 100%;
    }
  }

  &__title {
    font-size: 24px;
    letter-spacing: 2px;
    font-weight: 500;
    margin-bottom: 18px;
  }

  &__text {
    text-align: center;
    font-weight: 500;
  }
}
</style>
