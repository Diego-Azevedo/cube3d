<template>
  <section id="quem-somos" class="enterprise-section">
    <div class="content-container">
      
      <div class="main-grid">
        <div class="text-content">
          <span class="eyebrow">NOSSA ESSÊNCIA</span>
          
          <p class="description">
            A <strong>Works Sistemas Inteligentes</strong> é especialista em entregar soluções que realmente funcionam.
            Fundada para resolver problemas reais de operação, atua com foco em segurança eletrônica, automação e sistemas
            inteligentes, utilizando exclusivamente tecnologia <strong>Hikvision</strong> para garantir confiabilidade, padronização e alto desempenho.
          </p>
          
          <p class="description">
            Desenvolvemos e gerenciamos sistemas profissionais de monitoramento por câmeras IP, controle de acesso, reconhecimento
            facial e automação, sempre com foco em inteligência artificial, segurança da informação e funcionamento contínuo no ambiente real.
          </p>

          <p class="description">
            A atuação da Works é guiada por um padrão técnico rigoroso. Trabalhamos exclusivamente com soluções IP, descartando sistemas
            analógicos, com arquitetura bem definida e acompanhamento contínuo. Todas as decisões técnicas são baseadas em experiência prática de campo, garantindo
            que a tecnologia entregue funcione de forma confiável ao longo do tempo.
          </p>

          <div class="actions">
            <button class="btn-primary">Solicitar Consultoria</button>
          </div>
        </div>

        <div class="segments-display">
          <span class="eyebrow-small">SEGMENTOS ATENDIDOS</span>
          
          <div class="segments-column">
            <div 
              v-for="(segment, index) in segments" 
              :key="index" 
              class="segment-card"
            >
              <div class="card-bg" :style="{ backgroundImage: `url(${segment.image})` }"></div>

              <div class="segment-overlay"></div>
              
              <div class="segment-info">
                <span class="segment-name">{{ segment.name }}</span>
                <div class="segment-indicator"></div>
              </div>
            </div>
          </div>
        </div>
      </div>

    </div>
  </section>
</template>

<script setup>
import imgResidencial from '../assets/segments/residence.jpg'
import imgCondominium from '../assets/segments/condominium.jpg'
import imgCam from '../assets/segments/cam.png'
import imgFactory from '../assets/segments/factory.jpg'

const segments = [
  { name: 'Residencial', image: imgResidencial },
  { name: 'Condomínios', image: imgCondominium },
  { name: 'Empresas e Comércios', image: imgCam },
  { name: 'Indústrias', image: imgFactory },
  { name: 'Obras e Canteiros', image: imgResidencial },
  { name: 'Estacionamentos', image: imgResidencial },
  { name: 'Frotas e Veículos Corporativos', image: imgResidencial },
]
</script>

<style scoped>
.enterprise-section {
  background-color: #000;
  color: #fff;
  min-height: 100vh;
  display: flex;
  align-items: center;
  padding: 120px 2rem;
  width: 100%;
}

.content-container {
  max-width: 1280px;
  margin: 0 auto;
  width: 100%;
}

.main-grid {
  display: grid;
  grid-template-columns: 1.1fr 0.9fr; /* Ajuste sutil na proporção */
  gap: 6rem;
  align-items: start; /* Alinhamento ao topo garantido */
}

/* --- Texto --- */
.eyebrow {
  color: #ba7928;
  font-size: 0.75rem;
  font-weight: 700;
  letter-spacing: 0.25em;
  display: block;
  margin-bottom: 2rem;
}

.eyebrow-small {
  color: #f8dd73;
  font-size: 0.65rem;
  font-weight: 800;
  letter-spacing: 0.15em;
  margin-bottom: 2rem; /* Alinhado com a margem do eyebrow da esquerda */
  display: block;
  opacity: 0.7;
}

.description {
  color: #9ca3af;
  font-size: 1.05rem;
  line-height: 1.8;
  margin-bottom: 1.8rem;
  max-width: 600px;
}

.btn-primary {
  background: linear-gradient(135deg, #ba7928, #f8dd73);
  color: #000;
  font-weight: 700;
  padding: 1.2rem 2.5rem;
  border-radius: 4px;
  border: none;
  cursor: pointer;
  transition: all 0.3s ease;
  text-transform: uppercase;
  font-size: 0.85rem;
}

/* --- Segmentos com Vídeo --- */
.segments-column {
  display: flex;
  flex-direction: column;
  gap: 12px;
}

.segment-card {
  position: relative;
  height: 58px; /* Altura original estreita */
  border-radius: 8px;
  overflow: hidden;
  border: 1px solid rgba(255, 255, 255, 0.08);
  transition: all 0.6s cubic-bezier(0.23, 1, 0.32, 1);
  cursor: pointer;
}

.card-bg {
  position: absolute;
  inset: 0;
  background-size: cover;
  background-position: center;
  transition: transform 0.6s ease, opacity 0.6s ease;
}

.segment-overlay {
  position: absolute;
  inset: 0;
  background: linear-gradient(90deg, #000000 30%, rgba(0, 0, 0, 0.2) 100%);
  z-index: 1;
}

.segment-info {
  position: relative;
  z-index: 2;
  height: 100%;
  display: flex;
  align-items: center;
  padding: 0 1.8rem;
}

.segment-name {
  font-size: 0.95rem;
  font-weight: 600;
  color: #fff;
  transition: all 0.4s;
}

.segment-indicator {
  height: 1px;
  width: 0;
  background: #f8dd73;
  margin-left: 1.2rem;
  transition: width 0.5s ease;
}

/* --- EXPANSÃO AO PASSAR O MOUSE --- */
.segment-card:hover {
  height: 160px; /* Aumentei a altura conforme solicitado */
  border-color: #ba7928;
  box-shadow: 0 15px 30px rgba(0, 0, 0, 0.5);
}

.segment-card:hover .card-bg {
  transform: scale(1.08);
  opacity: 0.7;
}

.segment-card:hover .segment-name {
  color: #f8dd73;
  transform: scale(1.1) translateX(10px);
}

.segment-card:hover .segment-indicator {
  width: 60px;
}

/* Mobile */
@media (max-width: 1024px) {
  .main-grid {
    grid-template-columns: 1fr;
    gap: 3rem;
  }
}
</style>