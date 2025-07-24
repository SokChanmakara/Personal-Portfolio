<script setup>
import { onMounted, ref } from "vue";

const isVisible = ref(false);

onMounted(() => {
  // Trigger animations on mount
  setTimeout(() => {
    isVisible.value = true;
  }, 100);

  // Add intersection observer for feature cards
  const observer = new IntersectionObserver(
    (entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.add("animate-in");
        }
      });
    },
    {
      threshold: 0.1,
      rootMargin: "0px 0px -50px 0px",
    }
  );

  // Observe feature cards
  setTimeout(() => {
    const cards = document.querySelectorAll(".feature-card");
    cards.forEach((card) => {
      observer.observe(card);
    });
  }, 500);
});
</script>

<template>
  <div class="welcome-section">
    <div class="welcome-text" :class="{ 'animate-fade-in': isVisible }">
      <h1 class="welcome-title">
        Hello, I'm <span class="highlight">Chanmakara</span>
      </h1>
      <h2 class="welcome-subtitle">SOFTWARE DEVELOPER</h2>
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
          <font-awesome-icon :icon="['fas', 'code']" />
        </div>
        <h3>Clean Code</h3>
        <p>
          Writing maintainable, scalable, and efficient code following best
          practices
        </p>
      </div>

      <div class="feature-card">
        <div class="feature-icon">
          <font-awesome-icon :icon="['fas', 'mobile-button']" />
        </div>
        <h3>Responsive Design</h3>
        <p>
          Creating beautiful interfaces that work seamlessly across all devices
        </p>
      </div>

      <div class="feature-card">
        <div class="feature-icon">
          <font-awesome-icon :icon="['fas', 'rocket']" />
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
  max-width: 1000px;
  width: 100%;
  overflow-x: hidden;
  background: linear-gradient(
    135deg,
    rgba(15, 23, 42, 0.1) 0%,
    rgba(30, 41, 59, 0.05) 100%
  );
}

.welcome-text {
  margin-bottom: 3rem;
  opacity: 0;
  transform: translateY(30px);
  transition: all 0.8s cubic-bezier(0.4, 0, 0.2, 1);
}

.welcome-text.animate-fade-in {
  opacity: 1;
  transform: translateY(0);
}

.welcome-title {
  font-size: 3.5rem;
  font-weight: 700;
  color: white;
  margin-bottom: 1rem;
  line-height: 1.2;
  animation: slideInFromLeft 1s ease-out 0.2s both;
}

.highlight {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  position: relative;
}

.highlight::after {
  content: "";
  position: absolute;
  bottom: -5px;
  left: 0;
  width: 0;
  height: 3px;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  border-radius: 2px;
  animation: expandWidth 1.5s ease-out 1.5s both;
}

.welcome-subtitle {
  font-size: 1.5rem;
  color: #64ffda;
  margin-bottom: 1.5rem;
  font-weight: 500;
  animation: slideInFromRight 1s ease-out 0.4s both;
  position: relative;
}

.welcome-subtitle::before {
  content: "< ";
  opacity: 0;
  animation: fadeIn 0.5s ease-out 1.8s both;
}

.welcome-subtitle::after {
  content: " />";
  opacity: 0;
  animation: fadeIn 0.5s ease-out 1.8s both;
}

.welcome-description {
  font-size: 1.2rem;
  color: #8892b0;
  line-height: 1.8;
  max-width: 600px;
  margin-bottom: 2rem;
  animation: slideInFromBottom 1s ease-out 0.6s both;
}

.cta-buttons {
  display: flex;
  gap: 1.5rem;
  margin-bottom: 3rem;
  flex-wrap: wrap;
  align-items: center;
  animation: slideInFromBottom 1s ease-out 0.8s both;
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
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  font-size: 1.1rem;
  min-width: 200px;
  white-space: nowrap;
  position: relative;
  overflow: hidden;
}

.cta-primary::before,
.cta-secondary::before {
  content: "";
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(
    90deg,
    transparent,
    rgba(255, 255, 255, 0.2),
    transparent
  );
  transition: left 0.6s ease;
}

.cta-primary:hover::before,
.cta-secondary:hover::before {
  left: 100%;
}

.cta-primary {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  box-shadow: 0 8px 25px rgba(102, 126, 234, 0.3);
}

.cta-primary:hover {
  transform: translateY(-3px) scale(1.02);
  box-shadow: 0 15px 35px rgba(102, 126, 234, 0.4);
  filter: brightness(1.1);
}

.cta-secondary {
  background: transparent;
  color: #64ffda;
  border: 2px solid #64ffda;
  box-shadow: 0 8px 25px rgba(100, 255, 218, 0.2);
}

.cta-secondary:hover {
  background: #64ffda;
  color: #0a192f;
  transform: translateY(-3px) scale(1.02);
  box-shadow: 0 15px 35px rgba(100, 255, 218, 0.4);
}

.feature-cards {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2rem;
}

.feature-card {
  background: linear-gradient(
    145deg,
    rgba(255, 255, 255, 0.05),
    rgba(255, 255, 255, 0.02)
  );
  backdrop-filter: blur(15px);
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: 1.5rem;
  padding: 2.5rem;
  text-align: center;
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  position: relative;
  overflow: hidden;
  opacity: 0;
  transform: translateY(50px);
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
}

.feature-card::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 3px;
  background: linear-gradient(90deg, #667eea, #764ba2, #64ffda);
  border-radius: 1.5rem 1.5rem 0 0;
  opacity: 0;
  transition: opacity 0.3s ease;
}

.feature-card:hover::before {
  opacity: 1;
}

.feature-card.animate-in {
  opacity: 1;
  transform: translateY(0);
}

.feature-card:nth-child(1).animate-in {
  animation: slideInFromBottom 0.8s ease-out 0.1s both;
}

.feature-card:nth-child(2).animate-in {
  animation: slideInFromBottom 0.8s ease-out 0.3s both;
}

.feature-card:nth-child(3).animate-in {
  animation: slideInFromBottom 0.8s ease-out 0.5s both;
}

.feature-card:hover {
  transform: translateY(-10px) scale(1.02);
  background: linear-gradient(
    145deg,
    rgba(255, 255, 255, 0.08),
    rgba(255, 255, 255, 0.03)
  );
  border-color: rgba(100, 255, 218, 0.4);
  box-shadow: 0 25px 50px rgba(0, 0, 0, 0.3);
}

.feature-icon {
  width: 4.5rem;
  height: 4.5rem;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  border-radius: 1.5rem;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0 auto 1.5rem;
  color: white;
  font-size: 1.8rem;
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  box-shadow: 0 8px 25px rgba(102, 126, 234, 0.3);
  position: relative;
  overflow: hidden;
}

.feature-icon::after {
  content: "";
  position: absolute;
  top: 50%;
  left: 50%;
  width: 0;
  height: 0;
  background: rgba(255, 255, 255, 0.2);
  border-radius: 50%;
  transform: translate(-50%, -50%);
  transition: all 0.4s ease;
}

.feature-card:hover .feature-icon {
  transform: scale(1.1) rotate(5deg);
  box-shadow: 0 15px 40px rgba(102, 126, 234, 0.4);
}

.feature-card:hover .feature-icon::after {
  width: 100%;
  height: 100%;
}

.feature-card h3 {
  color: white;
  font-size: 1.4rem;
  font-weight: 600;
  margin-bottom: 1rem;
  transition: color 0.3s ease;
}

.feature-card:hover h3 {
  color: #64ffda;
}

.feature-card p {
  color: #8892b0;
  line-height: 1.7;
  transition: color 0.3s ease;
}

.feature-card:hover p {
  color: #a0aec0;
}

/* Keyframe Animations */
@keyframes slideInFromLeft {
  from {
    opacity: 0;
    transform: translateX(-50px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes slideInFromRight {
  from {
    opacity: 0;
    transform: translateX(50px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes slideInFromBottom {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

@keyframes expandWidth {
  from {
    width: 0;
  }
  to {
    width: 100%;
  }
}

/* Responsive Design */
@media (max-width: 1024px) {
  .welcome-section {
    max-width: 100%;
    padding: 1.5rem;
  }

  .welcome-title {
    font-size: 3.5rem;
  }

  .feature-cards {
    grid-template-columns: repeat(3, 1fr);
    gap: 1.5rem;
  }

  .feature-card {
    padding: 2rem;
  }
}

@media (max-width: 768px) {
  .welcome-section {
    padding: 1.5rem;
  }

  .welcome-title {
    font-size: 2.5rem;
  }

  .cta-buttons {
    flex-direction: column;
    align-items: stretch;
    gap: 1rem;
  }

  .cta-primary,
  .cta-secondary {
    justify-content: center;
    min-width: 100%;
  }

  .feature-cards {
    grid-template-columns: 1fr;
    gap: 1.5rem;
  }

  .feature-card {
    padding: 2rem;
  }

  .feature-card h3 {
    font-size: 1.2rem;
  }

  .feature-card p {
    font-size: 0.875rem;
  }
}

@media (max-width: 640px) {
  .feature-cards {
    grid-template-columns: 1fr;
    gap: 1.25rem;
  }

  .feature-card {
    padding: 1.75rem;
  }

  .feature-icon {
    width: 3.5rem;
    height: 3.5rem;
    font-size: 1.4rem;
    margin-bottom: 1rem;
  }

  .feature-card h3 {
    font-size: 1.1rem;
    margin-bottom: 0.75rem;
  }

  .feature-card p {
    font-size: 0.8rem;
    line-height: 1.5;
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

  .cta-primary,
  .cta-secondary {
    padding: 1rem 2rem;
    font-size: 1rem;
  }

  .feature-cards {
    grid-template-columns: 1fr;
    gap: 1.25rem;
  }

  .feature-card {
    padding: 1.5rem;
  }

  .feature-icon {
    width: 3.5rem;
    height: 3.5rem;
    font-size: 1.3rem;
    margin-bottom: 1rem;
  }

  .feature-card h3 {
    font-size: 1.1rem;
    margin-bottom: 0.75rem;
  }

  .feature-card p {
    font-size: 0.9rem;
    line-height: 1.5;
  }
}

@media (max-width: 360px) {
  .feature-cards {
    gap: 1rem;
  }

  .feature-card {
    padding: 1.25rem;
  }

  .feature-icon {
    width: 3rem;
    height: 3rem;
    font-size: 1.2rem;
    margin-bottom: 0.75rem;
  }

  .feature-card h3 {
    font-size: 1rem;
    margin-bottom: 0.5rem;
  }

  .feature-card p {
    font-size: 0.85rem;
  }
}

/* Reduced motion accessibility */
@media (prefers-reduced-motion: reduce) {
  .welcome-text,
  .feature-card,
  .cta-primary,
  .cta-secondary,
  .feature-icon {
    transition: none;
    animation: none;
  }

  .welcome-text {
    opacity: 1;
    transform: none;
  }

  .feature-card {
    opacity: 1;
    transform: none;
  }
}
</style>
