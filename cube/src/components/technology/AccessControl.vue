<template>
  <div id="tech-2" class="tech-detail-block">
    <div class="tech-container">
      
      <div class="tech-text-content">
        <div class="badge-ia">
          <span class="dot"></span>
          TECNOLOGIA TOUCHLESS HIKVISION
        </div>
        
        <h2 class="tech-title gradient-text">
          Controle de Acesso: <br />
          <span class="gradient-text">Biometria & IA</span>
        </h2>

        <p class="tech-description">
          Segurança sem fricção. Implementamos ecossistemas de acesso que combinam algoritmos de deep learning com a conveniência do fluxo contínuo.
        </p>

        <div class="tech-features-list">
          <div class="feature-item">
            <div class="feature-icon">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
                <path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm0 3c1.66 0 3 1.34 3 3s-1.34 3-3 3-3-1.34-3-3 1.34-3 3-3zm0 14.2c-2.5 0-4.71-1.28-6-3.22.03-1.99 4-3.08 6-3.08 1.99 0 5.97 1.09 6 3.08-1.29 1.94-3.5 3.22-6 3.22z" />
              </svg>
            </div>
            <div class="feature-info">
              <h4>Identificação Multi-Bio</h4>
              <p>Reconhecimento facial ultraveloz (&lt;0.2s), leitura de palma da mão (veias) e detecção de vivacidade (anti-spoofing).</p>
            </div>
          </div>

          <div class="feature-item">
            <div class="feature-icon">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
                <path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z" />
                <path d="M9 12l2 2 4-4" />
              </svg>
            </div>
            <div class="feature-info">
              <h4>Integração Operacional</h4>
              <p>Sincronização com bafômetros de precisão, bloqueio automático instantâneo e controle de perímetros (portões e cancelas).</p>
            </div>
          </div>

          <div class="feature-item">
            <div class="feature-icon">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
                <path d="M3 9l9-7 9 7v11a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z" />
                <polyline points="9 22 9 12 15 12 15 22" />
              </svg>
            </div>
            <div class="feature-info">
              <h4>Gestão em Nuvem & Auditoria</h4>
              <p>Dashboards em tempo real, gestão de permissões por níveis hierárquicos e relatórios completos de conformidade.</p>
            </div>
          </div>

          <div class="feature-item">
            <div class="feature-icon">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
                <rect x="3" y="11" width="18" height="11" rx="2" ry="2" />
                <path d="M7 11V7a5 5 0 0 1 10 0v4" />
              </svg>
            </div>
            <div class="feature-info">
              <h4>Versatilidade de Credenciais</h4>
              <p>Convergência total entre QR Code dinâmico, biometria, senha e reconhecimento de íris para áreas críticas.</p>
            </div>
          </div>
        </div>
      </div>

      <div class="tech-visual-content">
        <div class="image-glass-card">
          <div class="device-glow"></div>
          <img src="/src/assets/segments/minmoe.png" alt="Terminal Hikvision MinMoe" class="device-img" />
          
          <div class="floating-status-badge">
            <div class="status-indicator"></div>
            <div class="status-text">
              <span class="status-label">Status:</span>
              <span class="status-value">Acesso Autorizado</span>
            </div>
          </div>
        </div>
      </div>

    </div>
  </div>
</template>

<style scoped>
/* Estilos consistentes com Cftv.vue */
.tech-detail-block {
  padding: 60px 0;
  width: 100%;
  border-top: 1px solid rgba(255, 255, 255, 0.05);
}

.tech-container {
  max-width: 1280px;
  margin: 0 auto;
  padding: 0 2rem;
  display: grid;
  grid-template-columns: 1.1fr 0.9fr;
  gap: 4rem;
  align-items: center;
}

.badge-ia {
  display: inline-flex;
  align-items: center;
  gap: 0.8rem;
  padding: 0.5rem 1rem;
  background: rgba(186, 121, 40, 0.1);
  border: 1px solid rgba(186, 121, 40, 0.3);
  border-radius: 50px;
  color: #f8dd73;
  font-size: 0.75rem;
  font-weight: 700;
  letter-spacing: 1px;
  margin-bottom: 2rem;
}

.dot {
  width: 6px;
  height: 6px;
  background-color: #ff1e00;
  border-radius: 50%;
  box-shadow: 0 0 5px #f80000;
  animation: pulse 2s infinite;
}

.tech-title {
  font-size: clamp(2.5rem, 4vw, 3.5rem);
  line-height: 1.1;
  font-weight: 800;
  margin-bottom: 1.5rem;
  color: #fff;
}

.gradient-text {
  background: linear-gradient(90deg, #f8dd73, #ba7928);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.tech-description {
  color: #9ca3af;
  font-size: 1.125rem;
  line-height: 1.6;
  margin-bottom: 2rem;
  max-width: 540px;
}

.tech-features-list {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.feature-item {
  display: flex;
  gap: 1rem;
  background: rgba(255, 255, 255, 0.03);
  padding: 1rem;
  border-radius: 12px;
  border: 1px solid rgba(255, 255, 255, 0.05);
  transition: all 0.3s ease;
}

.feature-item:hover {
  transform: translateX(10px);
  border-color: rgba(186, 121, 40, 0.4);
  background: rgba(255, 255, 255, 0.05);
}

.feature-icon {
  width: 40px;
  height: 40px;
  background: rgba(186, 121, 40, 0.1);
  border-radius: 8px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #f8dd73;
  flex-shrink: 0;
}

.feature-icon svg {
  width: 22px;
  height: 22px;
}

.feature-info h4 {
  color: #fff;
  margin-bottom: 0.3rem;
  font-size: 1rem;
  font-weight: 600;
}

.feature-info p {
  color: #9ca3af;
  font-size: 0.9rem;
  line-height: 1.5;
  margin: 0;
}

.image-glass-card {
  position: relative;
  background: radial-gradient(circle at center, rgba(30, 30, 30, 0.4) 0%, transparent 70%);
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100%;
  min-height: 400px;
}

.device-glow {
  position: absolute;
  width: 100%;
  height: 100%;
  background: radial-gradient(ellipse at center, rgba(248, 221, 115, 0.15) 0%, transparent 70%);
  filter: blur(40px);
  z-index: 1;
}

.device-img {
  width: 100%;
  max-width: 500px;
  z-index: 2;
  position: relative;
  filter: drop-shadow(0 20px 50px rgba(248, 221, 115, 0.3));
  transition: transform 0.3s ease;
}

.device-img:hover {
  transform: scale(1.02);
}

.floating-status-badge {
  position: absolute;
  bottom: 15%;
  right: 5%;
  background: rgba(15, 15, 15, 0.85);
  backdrop-filter: blur(10px);
  border: 1px solid rgba(186, 121, 40, 0.3);
  padding: 1rem 1.5rem;
  border-radius: 12px;
  display: flex;
  align-items: center;
  gap: 1rem;
  z-index: 3;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.4);
  animation: float 3s ease-in-out infinite;
}

.status-indicator {
  width: 10px;
  height: 10px;
  background-color: #10b981;
  border-radius: 50%;
  box-shadow: 0 0 10px rgba(16, 185, 129, 0.6);
  animation: pulse-green 2s infinite;
}

.status-text {
  display: flex;
  flex-direction: column;
  gap: 0.2rem;
}

.status-label {
  font-size: 0.65rem;
  color: #ba7928;
  font-weight: 800;
  letter-spacing: 0.5px;
  text-transform: uppercase;
}

.status-value {
  font-size: 0.9rem;
  color: #fff;
  font-weight: 600;
}

@keyframes float {
  0%, 100% {
    transform: translateY(0px);
  }
  50% {
    transform: translateY(-10px);
  }
}

@keyframes pulse {
  0% { opacity: 0.5; transform: scale(1); }
  50% { opacity: 1; transform: scale(1.2); }
  100% { opacity: 0.5; transform: scale(1); }
}

@keyframes pulse-green {
  0%, 100% {
    opacity: 1;
    transform: scale(1);
  }
  50% {
    opacity: 0.7;
    transform: scale(1.2);
  }
}

@media (max-width: 1024px) {
  .tech-container {
    grid-template-columns: 1fr;
    text-align: center;
    gap: 3rem;
  }
  
  .feature-item {
    text-align: left;
  }
  
  .tech-visual-content {
    order: -1;
  }
  
  .tech-description {
    max-width: 100%;
  }
  
  .image-glass-card {
    min-height: 350px;
  }
  
  .tech-detail-block {
    padding: 40px 0;
  }
}
</style>
