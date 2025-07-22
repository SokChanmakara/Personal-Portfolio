<script setup>
// HomeView now just contains the welcome content
</script>

<template>
  <div class="welcome-section">
    <div class="welcome-text">
      <h1 class="welcome-title">
        Hello, I'm <span class="highlight">Chanmakara</span>
      </h1>
      <h2 class="welcome-subtitle">Full Stack Developer</h2>
      <p class="welcome-description">
        I create modern, responsive web applications using cutting-edge
        technologies. Passionate about clean code, user experience, and bringing
        innovative ideas to life.
      </p>

      <div class="cta-buttons">
        <router-link to="/portfolio" class="cta-primary">
          <i class="fas fa-briefcase"></i>
          View My Work
        </router-link>
        <router-link to="/contact" class="cta-secondary">
          <i class="fas fa-envelope"></i>
          Get In Touch
        </router-link>
      </div>
    </div>

    <!-- Feature Cards -->
    <div class="feature-cards">
      <div class="feature-card">
        <div class="feature-icon">
          <i class="fas fa-code"></i>
        </div>
        <h3>Clean Code</h3>
        <p>
          Writing maintainable, scalable, and efficient code following best
          practices
        </p>
      </div>

      <div class="feature-card">
        <div class="feature-icon">
          <i class="fas fa-mobile-alt"></i>
        </div>
        <h3>Responsive Design</h3>
        <p>
          Creating beautiful interfaces that work seamlessly across all devices
        </p>
      </div>

      <div class="feature-card">
        <div class="feature-icon">
          <i class="fas fa-rocket"></i>
        </div>
        <h3>Performance</h3>
        <p>
          Optimizing applications for speed, accessibility, and search engines
        </p>
      </div>
    </div>
  </div>
</template>

<style scoped>
.welcome-section {
  padding: 2rem;  
  min-height: 100%;
  width: 1000px;
  overflow-x: hidden;
}

.welcome-text {
  margin-bottom: 3rem;
}

.welcome-title {
  font-size: 3.5rem;
  font-weight: 700;
  color: white;
  margin-bottom: 1rem;
  line-height: 1.2;
}

.highlight {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.welcome-subtitle {
  font-size: 1.5rem;
  color: #64ffda;
  margin-bottom: 1.5rem;
  font-weight: 500;
}

.welcome-description {
  font-size: 1.2rem;
  color: #8892b0;
  line-height: 1.8;
  max-width: 600px;
  margin-bottom: 2rem;
}

.cta-buttons {
  display: flex;
  gap: 1.5rem;
  margin-bottom: 3rem;
  flex-wrap: wrap;
  align-items: center;
}

.cta-primary,
.cta-secondary {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 0.75rem;
  padding: 1.25rem 3rem;
  border-radius: 0.75rem;
  font-weight: 600;
  text-decoration: none;
  transition: all 0.3s ease;
  font-size: 1.1rem;
  min-width: 200px;
  white-space: nowrap;
}

.cta-primary {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
}

.cta-primary:hover {
  transform: translateY(-3px);
  box-shadow: 0 15px 35px rgba(102, 126, 234, 0.4);
  filter: brightness(1.1);
}

.cta-secondary {
  background: transparent;
  color: #64ffda;
  border: 2px solid #64ffda;
}

.cta-secondary:hover {
  background: #64ffda;
  color: #0a192f;
  transform: translateY(-3px);
  box-shadow: 0 15px 35px rgba(100, 255, 218, 0.3);
}

.feature-cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 2rem;
}

.feature-card {
  background: rgba(255, 255, 255, 0.05);
  backdrop-filter: blur(10px);
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: 1rem;
  padding: 2rem;
  text-align: center;
  transition: all 0.3s ease;
}

.feature-card:hover {
  transform: translateY(-8px);
  background: rgba(255, 255, 255, 0.08);
  border-color: rgba(100, 255, 218, 0.4);
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.2);
}

.feature-icon {
  width: 4rem;
  height: 4rem;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  border-radius: 1rem;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0 auto 1.5rem;
  color: white;
  font-size: 1.5rem;
}

.feature-card h3 {
  color: white;
  font-size: 1.25rem;
  font-weight: 600;
  margin-bottom: 1rem;
}

.feature-card p {
  color: #8892b0;
  line-height: 1.6;
}

/* Responsive Design */
@media (max-width: 768px) {
  .welcome-title {
    font-size: 2.5rem;
  }

  .cta-buttons {
    flex-direction: column;
    align-items: stretch;
  }

  .cta-primary,
  .cta-secondary {
    justify-content: center;
    min-width: 100%;
  }

  .feature-cards {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 480px) {
  .welcome-title {
    font-size: 2rem;
  }

  .welcome-description {
    font-size: 1rem;
  }

  .welcome-section {
    padding: 1rem;
  }
}
</style>
