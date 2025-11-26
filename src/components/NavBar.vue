<script setup lang="ts">
import { ref, onMounted, onUnmounted } from 'vue';

const isScrolled = ref(false);
const isMenuOpen = ref(false);

const handleScroll = () => {
  isScrolled.value = window.scrollY > 50;
};

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
};

onMounted(() => {
  window.addEventListener('scroll', handleScroll);
});

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll);
});

const scrollToSection = (id: string) => {
  const element = document.getElementById(id);
  if (element) {
    element.scrollIntoView({ behavior: 'smooth' });
    isMenuOpen.value = false;
  }
};
</script>

<template>
  <nav :class="['navbar', { 'scrolled': isScrolled }]">
    <div class="container">
      <div class="logo" @click="scrollToSection('hero')">
        Nex<span class="highlight">Vision</span>
      </div>
      
      <div class="menu-toggle" @click="toggleMenu">
        <span class="bar"></span>
        <span class="bar"></span>
        <span class="bar"></span>
      </div>

      <ul :class="['nav-links', { 'active': isMenuOpen }]">
        <li @click="scrollToSection('hero')">Home</li>
        <li @click="scrollToSection('about')">About</li>
        <li @click="scrollToSection('services')">Services</li>
        <li @click="scrollToSection('contact')">Contact</li>
      </ul>
    </div>
  </nav>
</template>

<style scoped>
.navbar {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  padding: 1.5rem 0;
  z-index: 1000;
  transition: all 0.3s ease;
  background: transparent;
}

.navbar.scrolled {
  background: rgba(10, 10, 20, 0.95);
  padding: 1rem 0;
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid rgba(255, 255, 255, 0.05);
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 2rem;
}

.logo {
  font-size: 1.8rem;
  font-weight: 700;
  color: #fff;
  cursor: pointer;
  letter-spacing: 1px;
}

.highlight {
  color: #00d4ff; /* Cyan accent */
}

.nav-links {
  display: flex;
  gap: 2.5rem;
  list-style: none;
}

.nav-links li {
  color: #e0e0e0;
  cursor: pointer;
  font-weight: 500;
  transition: color 0.3s ease;
  position: relative;
}

.nav-links li::after {
  content: '';
  position: absolute;
  width: 0;
  height: 2px;
  bottom: -5px;
  left: 0;
  background-color: #00d4ff;
  transition: width 0.3s ease;
}

.nav-links li:hover {
  color: #fff;
}

.nav-links li:hover::after {
  width: 100%;
}

.menu-toggle {
  display: none;
  flex-direction: column;
  gap: 5px;
  cursor: pointer;
}

.bar {
  width: 25px;
  height: 3px;
  background-color: #fff;
  transition: 0.3s;
}

@media (max-width: 768px) {
  .nav-links {
    position: absolute;
    top: 100%;
    left: 0;
    width: 100%;
    background: rgba(10, 10, 20, 0.98);
    flex-direction: column;
    align-items: center;
    padding: 2rem 0;
    gap: 2rem;
    transform: translateY(-150%);
    transition: transform 0.3s ease;
    z-index: -1;
  }

  .nav-links.active {
    transform: translateY(0);
  }

  .menu-toggle {
    display: flex;
  }
}
</style>
