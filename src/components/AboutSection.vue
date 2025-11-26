<script setup lang="ts">
</script>

<template>
  <section id="about" class="about-section">
    <div class="container">
      <div class="about-grid">
        <div class="about-text">
          <h2 class="section-title">Who We Are</h2>
          <p class="lead">
            NexVision is at the forefront of technological innovation, bridging the gap between imagination and reality.
          </p>
          <p class="description">
            We specialize in creating cutting-edge digital solutions that empower businesses to thrive in the modern era. From artificial intelligence to immersive web experiences, our team of experts is dedicated to pushing the boundaries of what's possible.
          </p>
          <div class="stats">
            <div class="stat-item">
              <span class="number">50+</span>
              <span class="label">Projects</span>
            </div>
            <div class="stat-item">
              <span class="number">15+</span>
              <span class="label">Experts</span>
            </div>
            <div class="stat-item">
              <span class="number">100%</span>
              <span class="label">Satisfaction</span>
            </div>
          </div>
        </div>
        <div class="about-visual">
          <div class="visual-card">
            <div class="card-content">
              <h3>Visionary</h3>
              <p>Thinking beyond limits.</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.about-section {
  padding: 8rem 2rem;
  background: #0a0a14;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
}

.about-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
  align-items: center;
}

.section-title {
  font-size: 2.5rem;
  margin-bottom: 2rem;
  color: #fff;
  position: relative;
  display: inline-block;
}

.section-title::after {
  content: '';
  position: absolute;
  bottom: -10px;
  left: 0;
  width: 60px;
  height: 4px;
  background: #00d4ff;
  border-radius: 2px;
}

.lead {
  font-size: 1.25rem;
  color: #e0e0e0;
  margin-bottom: 1.5rem;
  line-height: 1.6;
}

.description {
  color: #a0a0a0;
  margin-bottom: 3rem;
  line-height: 1.8;
}

.stats {
  display: flex;
  gap: 3rem;
}

.stat-item {
  display: flex;
  flex-direction: column;
}

.number {
  font-size: 2.5rem;
  font-weight: 700;
  color: #00d4ff;
}

.label {
  color: #808080;
  font-size: 0.9rem;
  text-transform: uppercase;
  letter-spacing: 1px;
}

.visual-card {
  background: linear-gradient(135deg, #1a1a2e, #16213e);
  border-radius: 20px;
  padding: 3rem;
  position: relative;
  overflow: hidden;
  border: 1px solid rgba(255, 255, 255, 0.05);
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
}

.visual-card::before {
  content: '';
  position: absolute;
  top: -50%;
  left: -50%;
  width: 200%;
  height: 200%;
  background: radial-gradient(circle, rgba(0, 212, 255, 0.1) 0%, transparent 70%);
  animation: rotate 20s linear infinite;
}

.card-content {
  position: relative;
  z-index: 1;
  text-align: center;
}

.card-content h3 {
  font-size: 2rem;
  color: #fff;
  margin-bottom: 0.5rem;
}

.card-content p {
  color: #00d4ff;
}

@keyframes rotate {
  from { transform: rotate(0deg); }
  to { transform: rotate(360deg); }
}

@media (max-width: 768px) {
  .about-grid {
    grid-template-columns: 1fr;
    gap: 3rem;
  }
}
</style>
