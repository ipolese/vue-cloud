<template>
  <header class="site-header">
    <div class="logo-container">
      <img src="../assets/logo.png" alt="Logo Igor Polese" class="logo">
    </div>
    <nav class="main-nav">
      <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#about">Sobre mim</a></li>
        <li><a href="#contact">Contato</a></li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'SiteHeader'
};
</script>

<style scoped>
.site-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px 40px; /* Ajuste o padding conforme necessário */
  position: fixed; /* Cabeçalho fixo no topo */
  top: 0;
  left: 0;
  width: 100%;
  box-sizing: border-box; /* Para o padding não aumentar a largura total */
  z-index: 1000; /* Para ficar sobre outros conteúdos */
  background-color: rgba(0,0,0,0.5); /* Um leve fundo para o header para destacar da imagem de fundo */
}

.logo {
  height: 50px; /* Ajuste conforme o tamanho do seu logo */
}

.main-nav ul {
  list-style: none;
  margin: 0;
  padding: 0;
  display: flex;
}

.main-nav li {
  margin-left: 30px; /* Espaçamento entre itens do menu */
}

.main-nav a {
  text-decoration: none;
  color: #DEDEDE;
  font-weight: bold;
  font-size: 1em;
  transition: color 0.3s ease;
}

.main-nav a:hover {
  color: #FFFFFF; /* Um pouco mais claro no hover */
}
</style>
