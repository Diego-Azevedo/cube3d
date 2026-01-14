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
      <section id="home" class="section home-section">
        <Home />
      </section>

      <!-- Seção Quem somos -->
      <section id="quem-somos" class="section">
        <div class="section-content">
          <h1>Quem somos</h1>
          <p>Conteúdo da seção Quem somos</p>
        </div>
      </section>

      <!-- Seção Nossos Serviços -->
      <section id="nossos-servicos" class="section">
        <div class="section-content">
          <h1>Nossos Serviços</h1>
          <p>Conteúdo da seção Nossos Serviços</p>
        </div>
      </section>

      <!-- Seção Tecnologia -->
      <section id="tecnologia" class="section">
        <div class="section-content">
          <h1>Tecnologia</h1>
          <p>Conteúdo da seção Tecnologia</p>
        </div>
      </section>

      <!-- Seção Depoimentos -->
      <section id="depoimentos" class="section">
        <div class="section-content">
          <h1>Depoimentos</h1>
          <p>Conteúdo da seção Depoimentos</p>
        </div>
      </section>

      <!-- Seção Contato -->
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

<style>
/* Reset global */
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
}
</style>

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
  background-color: rgba(0, 0, 0, 0.95);
  backdrop-filter: blur(10px);
  box-shadow: 0 2px 20px rgba(0, 0, 0, 0.3);
  z-index: 1000;
  padding: 1rem 0;
}

/* Navegação */
.nav {
  width: 100%;
  max-width: 1440px;
  margin: 0 auto;
  padding: 0 2rem;
}

.nav-list {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 2.5rem;
  list-style: none;
  margin: 0;
  padding: 0;
}

.nav-list li a {
  color: #f8dd73;
  text-decoration: none;
  font-weight: 500;
  font-size: 0.95rem;
  transition: all 0.3s ease;
  cursor: pointer;
  position: relative;
}

.nav-list li a::after {
  content: '';
  position: absolute;
  bottom: -4px;
  left: 0;
  width: 0;
  height: 2px;
  background: linear-gradient(90deg, #ba7928, #f8dd73);
  transition: width 0.3s ease;
}

.nav-list li a:hover {
  color: #ba7928;
}

.nav-list li a:hover::after {
  width: 100%;
}

/* Conteúdo principal */
.main-content {
  width: 100%;
}

/* Seções */
.section {
  width: 100%;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  box-sizing: border-box;
  position: relative;
}

/* Seção Home não precisa de padding ou overflow handling especial */
.home-section {
  padding: 0;
  background: #000;
}

/* Conteúdo das outras seções */
.section-content {
  max-width: 1200px;
  padding: 0 2rem;
  text-align: center;
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

/* Estilização alternada das seções */
.section:nth-child(2) {
  background-color: #f8f9fa;
}

.section:nth-child(3) {
  background-color: #ffffff;
}

.section:nth-child(4) {
  background-color: #f8f9fa;
}

.section:nth-child(5) {
  background-color: #ffffff;
}

.section:nth-child(6) {
  background-color: #f8f9fa;
}

/* Responsividade */
@media (max-width: 768px) {
  .nav-list {
    gap: 1.5rem;
    flex-wrap: wrap;
  }

  .nav-list li a {
    font-size: 0.85rem;
  }

  .section-content h1 {
    font-size: 2rem;
  }

  .section-content p {
    font-size: 1rem;
  }
}

@media (max-width: 480px) {
  .header {
    padding: 0.75rem 0;
  }

  .nav {
    padding: 0 1rem;
  }

  .nav-list {
    gap: 1rem;
    flex-wrap: wrap;
    justify-content: center;
  }

  .nav-list li a {
    font-size: 0.75rem;
  }

  .section-content h1 {
    font-size: 1.5rem;
  }
}
</style>