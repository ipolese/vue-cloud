<template>
  <div id="app-container">
    <SiteHeader />
    <MainContent />
  </div>
</template>

<script>
import SiteHeader from './components/SiteHeader.vue';
import MainContent from './components/MainContent.vue';

export default {
  name: 'App',
  components: {
    SiteHeader,
    MainContent
  }
};
</script>

<style>
/* Estilos Globais */
body {
  margin: 0;
  padding: 0;
  background-color: rgba(0, 0, 0, 0.8); /* Fallback */
  background-image: url('./assets/code2-bg.jpg');
  background-size: cover;
  background-position: center;
  background-attachment: fixed; /* Para a imagem ficar fixa durante o scroll */
  color: #DEDEDE;
  font-family: Helvetica, Arial, sans-serif; /* Helvetica primeiro, Arial como fallback comum */
  line-height: 1.6;
}

#app-container {
  /* Se necessário, um container geral para aplicar algum espaçamento ou limitar largura máxima no futuro */
}

/* Estilos para scroll suave para as âncoras */
html {
  scroll-behavior: smooth;
}
</style>
