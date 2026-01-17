<template>
  <div class="app-container">
    
    <Header />

    <main class="main-content">
      <section id="home" class="section home-section">
        <Home />
      </section>

      <section id="quem-somos" class="section">
        <div class="section-content">
          <h1>Quem somos</h1>
          <p>Conteúdo da seção Quem somos</p>
        </div>
      </section>

      <section id="nossos-servicos" class="section">
        <div class="section-content">
          <h1>Nossos Serviços</h1>
          <p>Conteúdo da seção Nossos Serviços</p>
        </div>
      </section>

      <section id="tecnologia" class="section">
        <div class="section-content">
          <h1>Tecnologia</h1>
          <p>Conteúdo da seção Tecnologia</p>
        </div>
      </section>

      <section id="depoimentos" class="section">
        <div class="section-content">
          <h1>Depoimentos</h1>
          <p>Conteúdo da seção Depoimentos</p>
        </div>
      </section>

      <section id="contato" class="section">
        <div class="section-content">
          <h1>Contato</h1>
          <p>Conteúdo da seção Contato</p>
        </div>
      </section>
    </main>
  </div>
</template>

<script setup>
import Header from './components/Header.vue'
import Home from './components/Home.vue'
</script>

<style>
/* Reset global e Smooth Scroll nativo */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  overflow-x: hidden;
  font-family: 'Inter', sans-serif; /* Sugestão de fonte moderna */
}
</style>

<style scoped>
/* Container principal */
.app-container {
  width: 100%;
  min-height: 100vh;
  position: relative;
}

/* Main Content */
.main-content {
  width: 100%;
}

/* Configuração geral das Seções */
.section {
  width: 100%;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
}

.home-section {
  padding: 0;
  background: #000;
}

.section-content {
  max-width: 1200px;
  padding: 0 2rem;
  text-align: center;
  /* Espaçamento superior para compensar o header fixo se necessário, 
     embora o align-items: center centralize tudo verticalmente */
}

.section-content h1 {
  font-size: 3rem;
  color: #333;
  margin-bottom: 1.5rem;
}

.section-content p {
  font-size: 1.125rem;
  color: #666;
  line-height: 1.6;
}

/* Backgrounds alternados */
.section:nth-child(even) {
  background-color: #f8f9fa;
}

.section:nth-child(odd):not(.home-section) {
  background-color: #ffffff;
}

/* Responsividade Geral */
@media (max-width: 768px) {
  .section-content h1 {
    font-size: 2rem;
  }
  .section-content p {
    font-size: 1rem;
  }
}
</style>