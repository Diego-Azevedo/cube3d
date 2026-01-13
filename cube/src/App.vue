<template>
  <div class="app-container">
    <!-- Header fixo no topo -->
    <header class="header">
      <nav class="nav">
        <ul class="nav-list">
          <li>
            <a href="#home" @click.prevent="scrollToSection('home')">Home</a>
          </li>
          <li>
            <a href="#quem-somos" @click.prevent="scrollToSection('quem-somos')">Quem somos</a>
          </li>
          <li>
            <a href="#nossos-servicos" @click.prevent="scrollToSection('nossos-servicos')">Nossos Serviços</a>
          </li>
          <li>
            <a href="#tecnologia" @click.prevent="scrollToSection('tecnologia')">Tecnologia</a>
          </li>
          <li>
            <a href="#depoimentos" @click.prevent="scrollToSection('depoimentos')">Depoimentos</a>
          </li>
          <li>
            <a href="#contato" @click.prevent="scrollToSection('contato')">Contato</a>
          </li>
        </ul>
      </nav>
    </header>

    <!-- Conteúdo principal com seções -->
    <main class="main-content">
      <!-- Seção Home -->
      <section id="home" class="section">
        <!-- <Camera360/> -->
        <Home/>
      </section>

      <!-- Seção Quem somos -->
      <section id="quem-somos" class="section">
        <h1>Quem somos</h1>
      </section>

      <!-- Seção Nossos Serviços -->
      <section id="nossos-servicos" class="section">
        <h1>Nossos Serviços</h1>
      </section>

      <!-- Seção Tecnologia -->
      <section id="tecnologia" class="section">
        <h1>Tecnologia</h1>
      </section>

      <!-- Seção Depoimentos -->
      <section id="depoimentos" class="section">
        <h1>Depoimentos</h1>
      </section>

      <!-- Seção Contato -->
      <section id="contato" class="section">
        <h1>Contato</h1>
      </section>
    </main>
  </div>
</template>

<script setup>
// import Camera360 from './components/Camera360.vue'
import Home from './components/Home.vue'
/**
 * Função para rolar suavemente até uma seção específica
 * @param {string} sectionId - ID da seção de destino
 */
const scrollToSection = (sectionId) => {
  const element = document.getElementById(sectionId);
  if (element) {
    element.scrollIntoView({
      behavior: 'smooth',
      block: 'start'
    });
  }
};
</script>

<style scoped>
/* Container principal */
.app-container {
  width: 100%;
  min-height: 100vh;
  position: relative;
}

/* Header fixo */
.header {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  width: 100%;
  background-color: rgba(255, 255, 255, 0.95);
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
  z-index: 1000;
  padding: 1rem 0;
}

/* Navegação */
.nav {
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
}

.nav-list {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 2rem;
  list-style: none;
  margin: 0;
  padding: 0;
}

.nav-list li a {
  color: #333;
  text-decoration: none;
  font-weight: 500;
  font-size: 1rem;
  transition: color 0.3s ease;
  cursor: pointer;
}

.nav-list li a:hover {
  color: #007bff;
}

/* Conteúdo principal */
.main-content {
  width: 100%;
  padding-top: 60px; /* Espaço para o header fixo */
}

/* Seções */
.section {
  width: 100%;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  box-sizing: border-box;
}

/* Estilização alternada das seções para melhor visualização */
.section:nth-child(odd) {
  background-color: #f8f9fa;
}

.section:nth-child(even) {
  background-color: #ffffff;
}

.section h1 {
  font-size: 3rem;
  color: #333;
  text-align: center;
  margin: 0;
}
</style>
