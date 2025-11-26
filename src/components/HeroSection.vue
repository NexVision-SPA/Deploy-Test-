<script setup lang="ts">
</script>

<template>
  <section id="hero" class="hero-section">
    <div class="hero-content">
      <h1 class="headline">Innovating the <span class="highlight">Future</span></h1>
      <p class="subheadline">Advanced Technology Solutions for Tomorrow's World - IA</p>
      <div class="cta-group">
        <button class="btn primary">Get Started</button>
        <button class="btn secondary">Learn More</button>
      </div>
    </div>
    <div class="hero-background">
      <div class="glow-orb orb-1"></div>
      <div class="glow-orb orb-2"></div>
    </div>
  </section>
</template>

<style scoped>
.hero-section {
  position: relative;
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden;
  padding: 0 2rem;
}

.hero-content {
  text-align: center;
  z-index: 10;
  max-width: 800px;
}

.headline {
  font-size: 4rem;
  font-weight: 800;
  margin-bottom: 1.5rem;
  line-height: 1.1;
  background: linear-gradient(to right, #ffffff, #a0a0a0);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  animation: fadeInUp 1s ease-out;
}

.highlight {
  background: linear-gradient(to right, #00d4ff, #005bea);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.subheadline {
  font-size: 1.5rem;
  color: #b0b0b0;
  margin-bottom: 3rem;
  animation: fadeInUp 1s ease-out 0.2s backwards;
}

.cta-group {
  display: flex;
  gap: 1.5rem;
  justify-content: center;
  animation: fadeInUp 1s ease-out 0.4s backwards;
}

.btn {
  padding: 1rem 2.5rem;
  border-radius: 50px;
  font-size: 1.1rem;
  font-weight: 600;
  cursor: pointer;
  transition: all 0.3s ease;
  border: none;
}

.btn.primary {
  background: linear-gradient(135deg, #00d4ff, #005bea);
  color: #fff;
  box-shadow: 0 10px 20px rgba(0, 212, 255, 0.3);
}

.btn.primary:hover {
  transform: translateY(-3px);
  box-shadow: 0 15px 30px rgba(0, 212, 255, 0.4);
}

.btn.secondary {
  background: transparent;
  border: 2px solid rgba(255, 255, 255, 0.2);
  color: #fff;
}

.btn.secondary:hover {
  background: rgba(255, 255, 255, 0.1);
  border-color: #fff;
}

.hero-background {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 1;
}

.glow-orb {
  position: absolute;
  border-radius: 50%;
  filter: blur(100px);
  opacity: 0.4;
}

.orb-1 {
  width: 400px;
  height: 400px;
  background: #005bea;
  top: -100px;
  left: -100px;
  animation: float 10s infinite ease-in-out;
}

.orb-2 {
  width: 500px;
  height: 500px;
  background: #00d4ff;
  bottom: -150px;
  right: -150px;
  animation: float 12s infinite ease-in-out reverse;
}

@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes float {
  0%, 100% {
    transform: translate(0, 0);
  }
  50% {
    transform: translate(30px, 50px);
  }
}

@media (max-width: 768px) {
  .headline {
    font-size: 2.5rem;
  }
  .subheadline {
    font-size: 1.2rem;
  }
  .cta-group {
    flex-direction: column;
  }
}
</style>
