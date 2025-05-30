<template>
  <main class="main-content">
    <section id="home" class="home-section section">
      <div class="home-content">
        <div class="home-text">
          <h1>Desenvolvedor Full Stack Sênior</h1>
          <h2>Tech Lead</h2>
          <p class="name">Igor Polese</p>
        </div>
        <div class="home-photo">
          <img src="../assets/profile.jpg" alt="Igor Polese" class="profile-picture">
        </div>
      </div>
    </section>

    <section id="about" class="about-section section">
      <div class="section-container">
        <h2>Sobre mim</h2>
        <div class="about-content-wrapper">
          <!-- O título já está acima, o texto abaixo ocupará a largura -->
          <p>Sou um desenvolvedor Full Stack criativo e bem humorado, com mais de 12 anos de experiência em desenvolvimento web e mobile. Trabalhei em algumas empresas de grande porte dentro e fora do Brasil e tenho experiência em diversas linguagens, interfaces, frameworks e bibliotecas, como PHP, Codeigniter, Laravel, Javascript, Vue.js, jQuery, React, Node.js, TypeScript, HTML e CSS, WordPress, Magento, Java e C. Além disso, tenho conhecimentos em áreas como OOP, Front-End, Back-End, MySQL, MongoDB e Scrum.</p>
          <p>Acredito firmemente no poder da tecnologia para impulsionar mudanças e estou constantemente buscando maneiras de aprimorar minhas habilidades e conhecimentos. Nos momentos de folga, valorizo o tempo com minha família, desfruto da mecânica automotiva, me envolvo em projetos manuais, acompanho séries e sou um entusiasta quando se trata de explorar diferentes tipos de cafés, cervejas artesanais e vinhos. Minha paixão pelo café é tão intensa que, em 2023, realizei um grande sonho ao adquirir uma cafeteria junto com minha esposa, dando vida ao nosso projeto paralelo, a Cafezar Cafeteria.</p>
          <p>Sinta-se à vontade para entrar em contato comigo para discutir projetos de desenvolvimento ou apenas para bater um papo!</p>
        </div>
      </div>
    </section>

    <section id="contact" class="contact-section section">
      <div class="section-container">
        <h2>Contatos</h2>
        <div class="contact-content-wrapper">
          <p>Me mande um e-mail</p>
          <p class="contact-detail"><a href="mailto:eu@igorpolese.com.br">eu@igorpolese.com.br</a></p>
          <p>ou ligue para mim</p>
          <p class="contact-detail">+55 27 99886 7266</p>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
export default {
  name: 'MainContent'
};
</script>

<style scoped>
.main-content {
  padding-top: 100px; /* Altura aproximada do header fixo + algum espaço */
}

.section {
  min-height: 80vh; /* Altura mínima para cada seção, para testar o scroll */
  padding: 40px;    /* Espaçamento interno das seções */
  display: flex;
  flex-direction: column;
  justify-content: center; /* Centraliza o conteúdo verticalmente na seção */
}

.section-container {
  max-width: 900px; /* Largura máxima para o conteúdo das seções */
  margin: 0 auto;   /* Centraliza o container */
  background-color: rgba(0,0,0,0.0); /* SEM fundo para as seções, texto direto na imagem de fundo da página */
                                     /* Se precisar de fundo para as seções, mude aqui. ex: rgba(0,0,0,0.7) */
  padding: 30px;
  border-radius: 8px; /* Opcional: se quiser bordas arredondadas caso adicione fundo */
}

/* Home Section */
.home-section {
  display: flex;
  align-items: center; /* Centraliza verticalmente o conteúdo da home-section */
  text-align: left;
}

.home-content {
  display: flex;
  align-items: center; /* Alinha itens (texto e foto) verticalmente */
  justify-content: space-around; /* Espaço entre texto e foto */
  width: 100%;
  max-width: 1200px; /* Aumenta a largura máxima para a seção home */
  margin: 0 auto;
}

.home-text {
  flex-basis: 50%; /* Ocupa metade do espaço */
  padding-right: 20px; /* Espaço à direita do texto */
}

.home-text h1 {
  font-size: 2.8em; /* Tamanho maior para o título principal */
  margin-bottom: 0.2em;
  font-weight: bold;
}

.home-text h2 {
  font-size: 2em;
  margin-bottom: 0.5em;
  font-weight: normal; /* Tech Lead pode ser mais leve */
}

.home-text .name {
  font-size: 1.8em;
  font-weight: bold;
  margin-top: 0.5em;
}

.home-photo {
  flex-basis: 40%; /* Ocupa 40% do espaço */
  text-align: right; /* Alinha a foto à direita dentro do seu container */
}

.profile-picture {
  max-width: 350px; /* Ajuste o tamanho da foto de perfil */
  height: auto;
  border-radius: 50%; /* Foto redonda */
  border: 3px solid #DEDEDE; /* Borda clara na foto */
}

/* About and Contact Sections */
.about-section h2, .contact-section h2 {
  font-size: 2.2em;
  margin-bottom: 30px;
  text-align: left; /* Título da seção à esquerda */
  border-bottom: 2px solid #DEDEDE; /* Linha abaixo do título da seção */
  padding-bottom: 10px;
}

.about-content-wrapper p, .contact-content-wrapper p {
  margin-bottom: 15px;
  font-size: 1.1em;
}

.contact-detail {
  font-weight: bold;
}

.contact-detail a {
  color: #DEDEDE;
  text-decoration: none;
  transition: color 0.3s ease;
}

.contact-detail a:hover {
  color: #FFFFFF;
  text-decoration: underline;
}

/* Ajustes para telas menores */
@media (max-width: 768px) {
  .site-header {
    padding: 15px 20px;
  }
  .main-nav ul {
    flex-direction: column; /* Menu hamburguer seria o ideal, mas para simplificar... */
    align-items: flex-end;
  }
  .main-nav li {
    margin-left: 0;
    margin-top:10px;
  }

  .home-content {
    flex-direction: column; /* Empilha texto e foto em telas menores */
    text-align: center;
  }
  .home-text {
    padding-right: 0;
    margin-bottom: 30px;
  }
  .home-photo {
    text-align: center; /* Centraliza a foto */
    margin-top: 20px;
  }
  .profile-picture {
    max-width: 250px;
  }
  .section {
    padding: 20px;
  }
  .section-container{
    padding: 20px;
  }
}
</style>
