<template>
  <section class="hero-section">
    <!-- Camadas de fundo -->
    <div class="hero-bg">
      <div class="bg-radial"></div>
      <div class="bg-left"></div>
      <div class="bg-right"></div>
      <div class="bg-noise"></div>
    </div>

    <!-- Conteúdo -->
    <div class="hero-content">
      <!-- Texto (foreground) -->
      <div class="hero-text">
        <span class="hero-eyebrow">SOLUÇÕES DE SEGURANÇA</span>

        <h1>
          WORKS<br />
          <span>SISTEMAS INTELIGENTES</span>
        </h1>

        <p>
          O mais alto nível de tecnologia Hikvision em segurança,
          controle de acesso e gestão operacional.
        </p>

        <button class="hero-button">
          Conhecer agora
        </button>
      </div>

      <!-- Vídeo (background expandido) -->
      <div class="hero-video-bg">
        <video autoplay muted loop playsinline preload="metadata">
          <source src="/video/works2.mp4" type="video/mp4" />
        </video>
      </div>
    </div>
  </section>
</template>

<script setup>
/*
  Componente puramente visual.
*/
</script>

<style scoped>
/* =====================
   VARIÁVEIS DE MARCA
   ===================== */
.hero-section {
  --bg-base: #000000;
  --bg-secondary: #121212;

  --yellow-primary: #ba7928;
  --yellow-light: #f8dd73;
  --yellow-dark: #ba7928;

  --text-main: #f8dd73;
  --text-muted: #9ca3af;
}

/* =====================
   CONTAINER PRINCIPAL
   ===================== */
.hero-section {
  position: relative;
  width: 100%;
  height: 100vh;
  background: var(--bg-base);
  overflow: hidden;
  display: flex;
  align-items: center;
}

/* =====================
   BACKGROUND LAYERS
   ===================== */
.hero-bg {
  position: absolute;
  inset: 0;
  z-index: 1;
}

/* Luz central */
.bg-radial {
  position: absolute;
  inset: -30%;
  background: radial-gradient(
    circle at 65% 50%,
    rgba(248, 221, 115, 0.35),
    rgba(0, 0, 0, 0.95) 60%
  );
  animation: pulse 10s ease-in-out infinite;
}

/* Vinheta esquerda */
.bg-left {
  position: absolute;
  left: 0;
  top: 0;
  width: 40%;
  height: 100%;
  background: linear-gradient(
    to right,
    rgba(0, 0, 0, 0.85),
    transparent
  );
}

/* Vinheta direita */
.bg-right {
  position: absolute;
  right: 0;
  top: 0;
  width: 40%;
  height: 100%;
  background: linear-gradient(
    to left,
    rgba(0, 0, 0, 0.6),
    transparent
  );
}

/* Ruído */
.bg-noise {
  position: absolute;
  inset: 0;
  background-image: url('/noise.png');
  opacity: 0.04;
  mix-blend-mode: overlay;
  pointer-events: none;
}

/* =====================
   CONTEÚDO
   ===================== */
.hero-content {
  position: relative;
  z-index: 2;
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
}

/* =====================
   TEXTO (SEMPRE NA FRENTE)
   ===================== */
.hero-text {
  position: relative;
  z-index: 3;
  max-width: 640px;
  color: var(--text-main);
}

.hero-eyebrow {
  font-size: 0.75rem;
  letter-spacing: 0.18em;
  text-transform: uppercase;
  color: var(--yellow-light);
}

.hero-text h1 {
  margin: 1rem 0;
  font-size: clamp(3rem, 6vw, 6rem);
  line-height: 1.05;
}

.hero-text h1 span {
  background: linear-gradient(
    90deg,
    var(--yellow-light),
    var(--yellow-primary)
  );
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.hero-text p {
  max-width: 480px;
  color: var(--text-muted);
  margin-bottom: 2rem;
}

/* =====================
   BOTÃO
   ===================== */
.hero-button {
  background: linear-gradient(
    135deg,
    var(--yellow-primary),
    var(--yellow-dark)
  );
  color: #111;
  font-weight: 600;
  padding: 0.85rem 1.9rem;
  border-radius: 999px;
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.hero-button:hover {
  transform: translateY(-2px);
  box-shadow: 0 12px 35px rgba(216, 164, 51, 0.45);
}

/* =====================
   VÍDEO COMO BACKGROUND PARCIAL
   ===================== */
   .hero-video-bg {
    position: absolute;
    inset: -15%;

    z-index: 2;
    overflow: hidden;
    border-radius: 1.5rem;
    pointer-events: none;

    box-shadow: 0 30px 90px rgba(0, 0, 0, 0.9);
  }


.hero-video-bg video {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

/* Fade para legibilidade do texto */
.hero-video-bg::after {
  content: '';
  position: absolute;
  inset: 0;
  background: linear-gradient(
    to left,
    rgba(0, 0, 0, 0.0),
    rgba(0, 0, 0, 0.8)
  );
}

/* =====================
   ANIMAÇÃO
   ===================== */
@keyframes pulse {
  0% { opacity: 0.35; }
  50% { opacity: 0.5; }
  100% { opacity: 0.35; }
}

/* =====================
   RESPONSIVO
   ===================== */
   @media (max-width: 900px) {
  .hero-video-bg {
    inset: auto 0;
    top: 50%;
    transform: translateY(-50%);

    height: 80vh;
    max-height: 80vh;
  }

  .hero-text {
    text-align: center;
    margin: 0 auto;
  }

  .hero-text p {
    margin-left: auto;
    margin-right: auto;
  }
}
</style>
