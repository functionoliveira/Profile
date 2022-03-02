<template>
  <nav class="nav-menu">
    <menu-item label="Home" anchor="#home" />
    <menu-item label="Experiência" anchor="#experience" />
    <menu-item label="Referências" anchor="#reference" />
    <menu-item label="Contato" anchor="#contact" />
  </nav>
</template>

<script>
import MenuItem from '~/components/menu/MenuItem'
export default {
  components: { MenuItem }
}
</script>

<style>
.nav-menu {
  z-index: 2;
}
</style>
