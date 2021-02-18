<template>
  <nav class="nav-menu">
    <menu-item label="Home" anchor="#home" />
    <menu-item label="Experiência" anchor="#experience" />
    <menu-item label="Referências" anchor="#reference" />
    <menu-item label="Interesses" anchor="#interests" />
    <menu-item label="Contato" anchor="#contact" />
    <!-- <div class="nav-menu__item"><a href="#home">Home</a></div>
    <div class="nav-menu__item"><a href="#experience">Experiência</a></div>
    <div class="nav-menu__item"><a href="#reference">Referências</a></div>
    <div class="nav-menu__item"><a href="#interests">Interesses</a></div>
    <div class="nav-menu__item"><a href="#contact">Contato</a></div> -->
  </nav>
</template>

<script>
import MenuItem from '~/components/menu/MenuItem'
export default {
  components: { MenuItem }
}
</script>

<style>

</style>
