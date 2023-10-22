<!-- Renderiza o componente "formulario" dentro desta-->
<template>
  <Navbar :logo="logo_src" :alt="app_name"/>
  <router-view/>
  <Formulario/>
</template>

<!-- Registra o componente "formulario" e Define o nome do componente como "App" Html-->
<script>
import Navbar from './components/Navbar.vue'
import Formulario from './components/Formulario.vue'

export default {
  components: {
    Navbar,
    Formulario
  },
  data() {
    return {
      logo_src: "",
      alt: "logo Ativa Investimentos",
    };
  },
  // Chama a função quando o componente é criado
  // Adiciona um ouvinte para redimensionamento da tela
  created() {
    this.setLogoProps(); 
    window.addEventListener('resize', this.setLogoProps); 
  },
  methods: { 
    setLogoProps() { 
      if (window.innerWidth >= 960) {
        this.logo_src = "../public/img/ativa-logo-dark.b56df060.svg";
      } else {
        this.logo_src = "../public/img/ativa-logo-mobile.e0133254.svg";
      }
    },
  },
  beforeDestroy() {
    window.removeEventListener('resize', this.setLogoProps); 
  }
}
</script>


<!-- Estilos CSS --> 
<style scoped>
</style>


