<template>
  <section class="hero-section">
    <div class="hero-bg">
      <div class="bg-gradient-mesh"></div>
      <div class="bg-noise"></div>
    </div>

    <div class="hero-container">

      <!-- HERO VIDEO -->
      <div class="hero-video">
        <div class="video-glow"></div>

        <div class="video-wrapper">
          <video autoplay muted loop playsinline preload="metadata">
            <source src="/video/works3.mp4" type="video/mp4" />
          </video>
        </div>
      </div>

      <!-- HERO CONTENT -->
      <div class="hero-content">
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

    </div>
  </section>
</template>

<style>
  .hero-section {
  --bg-base: #00000036;
  --yellow-primary: #ba7928;
  --yellow-light: #f8dd73;
  --text-muted: #9ca3af;
  background: var(--bg-base);
  position: relative;
  overflow: hidden;
  display: flex;
  justify-content: center;
}

/* =====================
   BACKGROUND
   ===================== */
.hero-bg {
  position: absolute;
  inset: 0;
  z-index: 0;
}

.bg-gradient-mesh {
  position: absolute;
  inset: 0;
  background: radial-gradient(circle at 50% 30%, #000, #000 70%);
}

.bg-noise {
  position: absolute;
  inset: 0;
  opacity: 0.05;
}

/* =====================
   CONTAINER
   ===================== */
.hero-container {
  position: relative;
  z-index: 2;
  width: 100%;
  max-width: 1440px;
  padding: 120px 2rem 80px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

/* =====================
   VIDEO HERO
   ===================== */
.hero-video {
  position: relative;
  max-width: 100%;
  max-height: 30%;
  margin-bottom: 5rem;
}

.video-glow {
  position: absolute;
  inset: -10%;
  background: radial-gradient(
    circle,
    rgba(250, 138, 1, 0.247),
    transparent 60%
  );
  filter: blur(120px);
  z-index: 0;
}

.video-wrapper {
  position: relative;
  z-index: 1;
  max-width: 1100px;
  max-height: 150%;
  margin: 0 auto;

  
  -webkit-mask-image: 
    radial-gradient(ellipse at center, black 15%, transparent 85%),
    linear-gradient(to right, transparent 0%, black 20%, black 80%, transparent 100%),
    linear-gradient(to bottom, black 0%, black 60%, transparent 100%);

  mask-image: 
    radial-gradient(ellipse at center, black 15%, transparent 85%),
    linear-gradient(to right, transparent 0%, black 20%, black 80%, transparent 100%),
    linear-gradient(to bottom, black 0%, black 60%, transparent 100%);

  -webkit-mask-composite: source-in;
  mask-composite: intersect;
}

.video-wrapper video {
  width: 100%;
  display: block;
  object-fit: cover;
  mix-blend-mode: screen;
}

/* =====================
   CONTENT
   ===================== */
.hero-content {
  text-align: center;
  max-width: 760px;
}

.hero-eyebrow {
  display: block;
  font-size: 0.75rem;
  letter-spacing: 0.18em;
  color: var(--yellow-light);
  margin-bottom: 1.5rem;
}

.hero-content h1 {
  font-size: clamp(3rem, 5vw, 5.5rem);
  line-height: 1.05;
  color: var(--yellow-light);
  margin-bottom: 1.5rem;
  font-weight: 700;
}

.hero-content h1 span {
  background: linear-gradient(
    90deg,
    var(--yellow-light),
    var(--yellow-primary)
  );
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.hero-content p {
  font-size: 1.125rem;
  line-height: 1.6;
  color: var(--text-muted);
  margin-bottom: 3rem;
}

/* =====================
   BUTTON
   ===================== */
.hero-button {
  background: linear-gradient(
    135deg,
    var(--yellow-primary),
    var(--yellow-light)
  );
  color: #111;
  font-weight: 600;
  padding: 1rem 3rem;
  border-radius: 999px;
  border: none;
  cursor: pointer;
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.hero-button:hover {
  transform: translateY(-2px);
  box-shadow: 0 12px 35px rgba(186, 121, 40, 0.45);
}

/* =====================
   MOBILE
   ===================== */
@media (max-width: 768px) {
  .hero-container {
    padding-top: 90px;
  }

  .video-wrapper {
    -webkit-mask-image: linear-gradient(
      to bottom,
      black 30%,
      transparent 100%
    );
    mask-image: linear-gradient(
      to bottom,
      black 30%,
      transparent 100%
    );
  }

  .hero-content h1 {
    font-size: 3rem;
  }
}

</style>