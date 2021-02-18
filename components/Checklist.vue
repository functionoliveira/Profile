<template>
  <div class="checklist">
    <div class="checklist__item">
      <check-icon />
      Metodologias Ágeis
    </div>
    <div class="checklist__item">
      <check-icon />
      Princípios SOLID
    </div>
    <div class="checklist__item">
      <check-icon />
      Design Patterns
    </div>
  </div>
</template>

<script>
import CheckIcon from "~/icons/CheckIcon";
export default {
  components: { CheckIcon }
}
</script>

<style lang="scss" scoped>
.checklist {

  &__item {
    display: flex;
    align-content: center;
    align-items: center;
    background: linear-gradient(180deg, white 10%, #7ac2d4 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    margin-bottom: 6px;
    font-weight: 600;

    svg {
      width: 32px;
      height: 32px;
      margin-right: 12px;
    }
  }
}
</style>
