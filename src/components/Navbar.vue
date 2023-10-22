<template>
  <div class="nav">
    <!-- Logo Navbar-->
    <router-link to="/">
   <div data-v-e8645e48="" id="header-logo" class="header-logo">
      <a href="#">
        <img :src="logo" id="logo" class="logoImg" :alt="alt">
      </a>
    </div>

    </router-link>
    <!-- Icone "?"-->
    <div class="md-button-content">
      <i class="las la-question-circle"></i>
    </div>

    <!-- Icone  "ℹ️" -->
    <div class="md-button" >
      <div class="md-button-content">
        <i data-v-e8645e48="" class="las la-info-circle"></i><span data-v-e8645e48="" class="md-small-hide">Atendimento</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name:"Navbar",
  props: ["logo", "alt"]

}
</script>

<!-- Estilos CSS -->
<style scoped>


</style>