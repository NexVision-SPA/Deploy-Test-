<script setup lang="ts">
const services = [
  {
    title: 'Software Development',
    description: 'Custom tailored software solutions built to scale and perform.',
    icon: 'code'
  },
  {
    title: 'AI Solutions',
    description: 'Leveraging machine learning to unlock new business potential.',
    icon: 'brain'
  },
  {
    title: 'Cloud Computing',
    description: 'Secure and scalable cloud infrastructure for modern enterprises.',
    icon: 'cloud'
  },
  {
    title: 'Cyber Security',
    description: 'Protecting your digital assets with advanced security protocols.',
    icon: 'shield'
  }
];
</script>

<template>
  <section id="services" class="services-section">
    <div class="container">
      <h2 class="section-title">Our Services</h2>
      <div class="services-grid">
        <div v-for="(service, index) in services" :key="index" class="service-card">
          <div class="icon-wrapper">
            <!-- Simple CSS icons for demo purposes -->
            <div :class="['icon', service.icon]"></div>
          </div>
          <h3>{{ service.title }}</h3>
          <p>{{ service.description }}</p>
          <a href="#" class="learn-more">Learn More &rarr;</a>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.services-section {
  padding: 8rem 2rem;
  background: #0f0f1a;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
}

.section-title {
  font-size: 2.5rem;
  margin-bottom: 4rem;
  color: #fff;
  text-align: center;
}

.services-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
}

.service-card {
  background: #1a1a2e;
  padding: 2.5rem;
  border-radius: 15px;
  transition: all 0.3s ease;
  border: 1px solid rgba(255, 255, 255, 0.03);
  position: relative;
  overflow: hidden;
}

.service-card:hover {
  transform: translateY(-10px);
  background: #202035;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
  border-color: rgba(0, 212, 255, 0.2);
}

.icon-wrapper {
  margin-bottom: 1.5rem;
}

.icon {
  width: 50px;
  height: 50px;
  background: #00d4ff;
  border-radius: 10px;
  opacity: 0.8;
}

.icon.code { background: linear-gradient(135deg, #ff0080, #ff8c00); }
.icon.brain { background: linear-gradient(135deg, #7928ca, #ff0080); }
.icon.cloud { background: linear-gradient(135deg, #00d4ff, #005bea); }
.icon.shield { background: linear-gradient(135deg, #00f260, #0575e6); }

h3 {
  font-size: 1.5rem;
  color: #fff;
  margin-bottom: 1rem;
}

p {
  color: #a0a0a0;
  margin-bottom: 1.5rem;
  line-height: 1.6;
}

.learn-more {
  color: #00d4ff;
  text-decoration: none;
  font-weight: 600;
  transition: gap 0.3s ease;
  display: inline-flex;
  align-items: center;
  gap: 5px;
}

.service-card:hover .learn-more {
  gap: 10px;
}
</style>
