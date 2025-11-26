<script setup lang="ts">
</script>

<template>
  <footer id="contact" class="footer-section">
    <div class="container">
      <div class="footer-content">
        <div class="footer-brand">
          <h2>Nex<span class="highlight">Vision</span></h2>
          <p>Building the future, one line of code at a time.</p>
        </div>
        <div class="footer-links">
          <div class="link-group">
            <h4>Company</h4>
            <a href="#">About Us</a>
            <a href="#">Careers</a>
            <a href="#">Blog</a>
          </div>
          <div class="link-group">
            <h4>Resources</h4>
            <a href="#">Documentation</a>
            <a href="#">Support</a>
            <a href="#">Terms of Service</a>
          </div>
          <div class="link-group">
            <h4>Connect</h4>
            <a href="#">Twitter</a>
            <a href="#">LinkedIn</a>
            <a href="#">GitHub</a>
          </div>
        </div>
      </div>
      <div class="footer-bottom">
        <p>&copy; 2024 NexVision Technologies. All rights reserved.</p>
      </div>
    </div>
  </footer>
</template>

<style scoped>
.footer-section {
  background: #05050a;
  padding: 5rem 2rem 2rem;
  border-top: 1px solid rgba(255, 255, 255, 0.05);
}

.container {
  max-width: 1200px;
  margin: 0 auto;
}

.footer-content {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 4rem;
  margin-bottom: 4rem;
}

.footer-brand h2 {
  font-size: 2rem;
  color: #fff;
  margin-bottom: 1rem;
}

.highlight {
  color: #00d4ff;
}

.footer-brand p {
  color: #808080;
  max-width: 300px;
}

.footer-links {
  display: flex;
  gap: 4rem;
  flex-wrap: wrap;
}

.link-group h4 {
  color: #fff;
  margin-bottom: 1.5rem;
  font-size: 1.1rem;
}

.link-group a {
  display: block;
  color: #a0a0a0;
  text-decoration: none;
  margin-bottom: 0.8rem;
  transition: color 0.3s ease;
}

.link-group a:hover {
  color: #00d4ff;
}

.footer-bottom {
  text-align: center;
  padding-top: 2rem;
  border-top: 1px solid rgba(255, 255, 255, 0.05);
  color: #606060;
  font-size: 0.9rem;
}

@media (max-width: 768px) {
  .footer-content {
    flex-direction: column;
    gap: 3rem;
  }
  .footer-links {
    gap: 2rem;
    width: 100%;
    justify-content: space-between;
  }
}
</style>
