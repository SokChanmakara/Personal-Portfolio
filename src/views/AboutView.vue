<template>
  <div class="about-container">
    <!-- Header Section -->
    <div class="text-center mb-16" :class="{ 'animate-fade-in': isVisible }">
      <h1
        class="text-5xl font-bold mb-20 bg-gradient-to-r from-blue-400 via-purple-500 to-cyan-400 bg-clip-text text-transparent header-title"
      >
        About Me
      </h1>
      <div class="max-w-4xl mx-auto">
        <p
          class="text-xl text-gray-200 leading-relaxed mb-8 font-medium intro-text"
        >
          I'm a passionate Mobile & Web Application developer focused on
          building real-world projects using modern tools like Flutter and web
          technologies. I enjoy solving problems through clean code, thoughtful
          design, and continuous learning.
        </p>
        <p class="text-lg text-gray-300 leading-relaxed intro-text-2">
          I've built a variety of apps through personal and academic projects
          from simple tools to more complex applications.
        </p>
      </div>
    </div>

    <!-- Milestones & Achievements -->
    <div class="mb-16">
      <h2 class="section-title">🚀 Milestones & Achievements</h2>
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <div class="achievement-card">
          <div
            class="achievement-number text-6xl font-bold bg-gradient-to-r from-blue-400 to-blue-600 bg-clip-text text-transparent mb-4"
          >
            1+
          </div>
          <div class="text-xl font-bold mb-3 text-white">
            YEARS OF LEARNING & BUILDING
          </div>
          <p class="text-gray-300 leading-relaxed">
            Spent over a year mastering Flutter and modern web technologies
            through hands-on practice and personal projects.
          </p>
        </div>

        <div class="achievement-card">
          <div
            class="achievement-number text-6xl font-bold bg-gradient-to-r from-green-400 to-emerald-600 bg-clip-text text-transparent mb-4"
          >
            10+
          </div>
          <div class="text-xl font-bold mb-3 text-white">
            PERSONAL PROJECTS COMPLETED
          </div>
          <p class="text-gray-300 leading-relaxed">
            Built multiple mobile and web apps
          </p>
        </div>

        <div class="achievement-card">
          <div
            class="achievement-number text-6xl font-bold bg-gradient-to-r from-purple-400 to-pink-600 bg-clip-text text-transparent mb-4"
          >
            7+
          </div>
          <div class="text-xl font-bold mb-3 text-white">COMMUNITY</div>
          <p class="text-gray-300 leading-relaxed">
            Actively learning, collaborating, and sharing knowledge through
            online communities, open source, or coding groups.
          </p>
        </div>
      </div>
    </div>

    <!-- Strategic Implementation Pathway -->
    <div class="mb-16">
      <h2 class="second-section-title">Strategic Implementation Pathway</h2>
      <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
        <!-- Planning & Strategy -->
        <div class="pathway-card">
          <div class="pathway-icon">
            <font-awesome-icon
              icon="fa-solid fa-magnifying-glass"
              class="text-2xl"
            />
          </div>
          <div class="pathway-content">
            <h3 class="text-xl font-bold mb-4 text-white">
              Planning & Strategy
            </h3>
            <p class="text-gray-300 leading-relaxed">
              I analyze your goals, target users, and key features to create a
              roadmap for your app's success.
            </p>
          </div>
        </div>

        <!-- Pixel-Perfect UI/UX Design -->
        <div class="pathway-card">
          <div class="pathway-icon design">
            <font-awesome-icon icon="fa-solid fa-palette" class="text-2xl" />
          </div>
          <div class="pathway-content">
            <h3 class="text-xl font-bold mb-4 text-white">
              Pixel-Perfect UI/UX Design
            </h3>
            <p class="text-gray-300 leading-relaxed">
              I create intuitive, visually appealing, and user-friendly
              interfaces that enhance engagement and usability.
            </p>
          </div>
        </div>

        <!-- Efficient Development & Seamless Integration -->
        <div class="pathway-card">
          <div class="pathway-icon development">
            <font-awesome-icon icon="fa-solid fa-code" class="text-2xl" />
          </div>
          <div class="pathway-content">
            <h3 class="text-xl font-bold mb-4 text-white">
              Efficient Development & Seamless Integration
            </h3>
            <p class="text-gray-300 leading-relaxed">
              I build high-performance, scalable applications with clean,
              maintainable code. I integrate essential features like API
              connections, third-party services, and IAP to enhance
              functionality.
            </p>
          </div>
        </div>

        <!-- Launch & Post-Launch Support -->
        <div class="pathway-card">
          <div class="pathway-icon launch">
            <font-awesome-icon icon="fa-solid fa-rocket" class="text-2xl" />
          </div>
          <div class="pathway-content">
            <h3 class="text-xl font-bold mb-4 text-white">
              Launch & Post-Launch Support
            </h3>
            <p class="text-gray-300 leading-relaxed">
              I ensure a hassle-free deployment and provide ongoing updates,
              optimizations, and support to keep your app running flawlessly.
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { onMounted, ref } from "vue";

const isVisible = ref(false);

onMounted(() => {
  // Trigger initial animations
  setTimeout(() => {
    isVisible.value = true;
  }, 100);

  // Add intersection observer for cards
  const observer = new IntersectionObserver(
    (entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.add("animate-in");

          // Special handling for achievement cards counter animation
          if (entry.target.classList.contains("achievement-card")) {
            const numberElement = entry.target.querySelector(
              ".achievement-number"
            );
            if (numberElement) {
              animateCounter(numberElement);
            }
          }
        }
      });
    },
    {
      threshold: 0.2,
      rootMargin: "0px 0px -50px 0px",
    }
  );

  // Observe all animated elements
  setTimeout(() => {
    const cards = document.querySelectorAll(".achievement-card, .pathway-card");
    cards.forEach((card) => {
      observer.observe(card);
    });
  }, 500);
});

function animateCounter(element) {
  const target = parseInt(element.textContent);
  const duration = 2000;
  const start = performance.now();

  function update(currentTime) {
    const elapsed = currentTime - start;
    const progress = Math.min(elapsed / duration, 1);
    const easeOut = 1 - Math.pow(1 - progress, 3);
    const current = Math.floor(easeOut * target);

    element.textContent = current + "+";

    if (progress < 1) {
      requestAnimationFrame(update);
    }
  }

  requestAnimationFrame(update);
}
</script>

<style scoped>
.about-container {
  padding: 2rem;
  color: white;
  min-height: 100%;
  overflow-x: hidden;
  background: linear-gradient(
    135deg,
    rgba(15, 23, 42, 0.1) 0%,
    rgba(30, 41, 59, 0.05) 100%
  );
}

/* Header Animations */
.text-center {
  opacity: 0;
  transform: translateY(30px);
  transition: all 0.8s cubic-bezier(0.4, 0, 0.2, 1);
}

.text-center.animate-fade-in {
  opacity: 1;
  transform: translateY(0);
}

.header-title {
  animation: slideInFromTop 1s ease-out 0.2s both;
  position: relative;
}

.header-title::after {
  content: "";
  position: absolute;
  bottom: -10px;
  left: 50%;
  transform: translateX(-50%);
  width: 0;
  height: 4px;
  background: linear-gradient(90deg, #3b82f6, #8b5cf6, #06b6d4);
  border-radius: 2px;
  animation: expandFromCenter 1.5s ease-out 1.5s both;
}

.intro-text {
  margin-top: 16px;
  animation: slideInFromLeft 1s ease-out 0.6s both;
}

.intro-text-2 {
  animation: slideInFromRight 1s ease-out 0.8s both;
}

.section-title {
  font-size: 1.875rem;
  font-weight: 700;
  text-align: center;
  background: linear-gradient(to right, #34d399, #06b6d4);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  margin: 2.5rem 0;
  position: relative;
  animation: fadeIn 1s ease-out 1s both;
}

.section-title::before {
  content: "🚀";
  position: absolute;
  left: -2rem;
  animation: bounce 2s infinite 2s;
}

.second-section-title {
  font-size: 1.875rem;
  font-weight: 700;
  text-align: center;
  background: linear-gradient(to right, #3da1c9, #8cdabd);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  margin: 2.5rem 0;
  animation: fadeIn 1s ease-out 1s both;
}

.achievement-card {
  background: linear-gradient(
    145deg,
    rgba(99, 102, 241, 0.1) 0%,
    rgba(139, 92, 246, 0.05) 50%,
    rgba(59, 130, 246, 0.1) 100%
  );
  backdrop-filter: blur(15px);
  border: 1px solid rgba(99, 102, 241, 0.2);
  border-radius: 1.5rem;
  padding: 2.5rem;
  text-align: center;
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  position: relative;
  overflow: hidden;
  opacity: 0;
  transform: translateY(50px) scale(0.9);
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
}

.achievement-card::before {
  content: "";
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(
    90deg,
    transparent,
    rgba(255, 255, 255, 0.1),
    transparent
  );
  transition: left 0.6s ease;
}

.achievement-card:hover::before {
  left: 100%;
}

.achievement-card.animate-in {
  opacity: 1;
  transform: translateY(0) scale(1);
}

.achievement-card:nth-child(1).animate-in {
  animation: slideInScale 0.8s ease-out 0.1s both;
}

.achievement-card:nth-child(2).animate-in {
  animation: slideInScale 0.8s ease-out 0.3s both;
}

.achievement-card:nth-child(3).animate-in {
  animation: slideInScale 0.8s ease-out 0.5s both;
}

.achievement-card:hover {
  background: linear-gradient(
    145deg,
    rgba(99, 102, 241, 0.15) 0%,
    rgba(139, 92, 246, 0.1) 50%,
    rgba(59, 130, 246, 0.15) 100%
  );
  border-color: rgba(99, 102, 241, 0.4);
  transform: translateY(-8px) scale(1.02);
  box-shadow: 0 25px 50px rgba(99, 102, 241, 0.3);
}

.achievement-number {
  transition: transform 0.3s ease;
}

.achievement-card:hover .achievement-number {
  transform: scale(1.1);
}

.pathway-card {
  background: linear-gradient(
    145deg,
    rgba(255, 255, 255, 0.05) 0%,
    rgba(99, 102, 241, 0.03) 50%,
    rgba(255, 255, 255, 0.02) 100%
  );
  backdrop-filter: blur(15px);
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: 1.5rem;
  padding: 2.5rem;
  display: flex;
  align-items: flex-start;
  gap: 1.5rem;
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  position: relative;
  overflow: hidden;
  opacity: 0;
  transform: translateX(-50px);
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
}

.pathway-card::after {
  content: "";
  position: absolute;
  top: 0;
  right: 0;
  width: 4px;
  height: 0%;
  background: linear-gradient(180deg, #6366f1, #8b5cf6, #06b6d4);
  transition: height 0.4s ease;
}

.pathway-card:hover::after {
  height: 100%;
}

.pathway-card.animate-in {
  opacity: 1;
  transform: translateX(0);
}

.pathway-card:nth-child(1).animate-in {
  animation: slideInFromLeft 0.8s ease-out 0.1s both;
}

.pathway-card:nth-child(2).animate-in {
  animation: slideInFromRight 0.8s ease-out 0.2s both;
}

.pathway-card:nth-child(3).animate-in {
  animation: slideInFromLeft 0.8s ease-out 0.3s both;
}

.pathway-card:nth-child(4).animate-in {
  animation: slideInFromRight 0.8s ease-out 0.4s both;
}

.pathway-card:hover {
  background: linear-gradient(
    145deg,
    rgba(255, 255, 255, 0.08) 0%,
    rgba(99, 102, 241, 0.05) 50%,
    rgba(255, 255, 255, 0.03) 100%
  );
  border-color: rgba(99, 102, 241, 0.3);
  transform: translateY(-5px) scale(1.01);
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
}

.pathway-icon {
  width: 4rem;
  height: 4rem;
  background: linear-gradient(135deg, #6366f1 0%, #8b5cf6 100%);
  border-radius: 1rem;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  flex-shrink: 0;
  box-shadow: 0 8px 25px rgba(99, 102, 241, 0.3);
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  position: relative;
  overflow: hidden;
}

.pathway-icon::before {
  content: "";
  position: absolute;
  top: 50%;
  left: 50%;
  width: 0;
  height: 0;
  background: rgba(255, 255, 255, 0.3);
  border-radius: 50%;
  transform: translate(-50%, -50%);
  transition: all 0.4s ease;
}

.pathway-card:hover .pathway-icon {
  transform: scale(1.15) rotate(10deg);
  box-shadow: 0 15px 40px rgba(99, 102, 241, 0.5);
}

.pathway-card:hover .pathway-icon::before {
  width: 100%;
  height: 100%;
}

.pathway-icon.design {
  background: linear-gradient(135deg, #ec4899 0%, #f59e0b 100%);
  box-shadow: 0 8px 25px rgba(236, 72, 153, 0.3);
}

.pathway-card:hover .pathway-icon.design {
  box-shadow: 0 15px 40px rgba(236, 72, 153, 0.5);
}

.pathway-icon.development {
  background: linear-gradient(135deg, #06b6d4 0%, #10b981 100%);
  box-shadow: 0 8px 25px rgba(6, 182, 212, 0.3);
}

.pathway-card:hover .pathway-icon.development {
  box-shadow: 0 15px 40px rgba(6, 182, 212, 0.5);
}

.pathway-icon.launch {
  background: linear-gradient(135deg, #10b981 0%, #84cc16 100%);
  box-shadow: 0 8px 25px rgba(16, 185, 129, 0.3);
}

.pathway-card:hover .pathway-icon.launch {
  box-shadow: 0 15px 40px rgba(16, 185, 129, 0.5);
}

.pathway-content {
  flex: 1;
}

.pathway-content h3 {
  transition: color 0.3s ease;
}

.pathway-card:hover .pathway-content h3 {
  color: #64ffda;
}

.pathway-content p {
  transition: color 0.3s ease;
}

.pathway-card:hover .pathway-content p {
  color: #a0aec0;
}

/* Keyframe Animations */
@keyframes slideInFromTop {
  from {
    opacity: 0;
    transform: translateY(-50px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

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

@keyframes slideInScale {
  from {
    opacity: 0;
    transform: translateY(50px) scale(0.8);
  }
  to {
    opacity: 1;
    transform: translateY(0) scale(1);
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

@keyframes expandFromCenter {
  from {
    width: 0;
  }
  to {
    width: 120px;
  }
}

@keyframes bounce {
  0%,
  20%,
  50%,
  80%,
  100% {
    transform: translateY(0);
  }
  40% {
    transform: translateY(-10px);
  }
  60% {
    transform: translateY(-5px);
  }
}

@media (max-width: 1024px) {
  .about-container {
    padding: 1.5rem;
  }

  .header-title {
    font-size: 3.5rem;
  }

  .achievement-card {
    padding: 2.5rem;
  }

  .pathway-card {
    padding: 2rem;
  }

  .achievement-number {
    font-size: 4rem;
  }
}

@media (max-width: 768px) {
  .about-container {
    padding: 1rem;
  }

  .header-title {
    font-size: 2.5rem;
  }

  .intro-text {
    font-size: 1.1rem;
  }

  .intro-text-2 {
    font-size: 1rem;
  }

  .pathway-card {
    flex-direction: column;
    text-align: center;
    padding: 2rem;
  }

  .pathway-icon {
    margin: 0 auto 1rem auto;
  }

  .achievement-card {
    padding: 2rem;
    text-align: center;
  }

  .achievement-number {
    font-size: 3rem;
  }

  .section-title::before {
    position: static;
    margin-right: 1rem;
  }

  .section-title {
    font-size: 1.5rem;
  }

  .second-section-title {
    font-size: 1.5rem;
  }
}

@media (max-width: 480px) {
  .about-container {
    padding: 0.75rem;
  }

  .header-title {
    font-size: 2rem;
  }

  .intro-text {
    font-size: 1rem;
    margin-bottom: 1.5rem;
  }

  .intro-text-2 {
    font-size: 0.95rem;
  }

  .achievement-card {
    padding: 1.5rem;
  }

  .pathway-card {
    padding: 1.5rem;
  }

  .achievement-number {
    font-size: 2.5rem;
    margin-bottom: 0.75rem;
  }

  .pathway-icon {
    width: 3rem;
    height: 3rem;
    margin-bottom: 1rem;
  }

  .pathway-content h3 {
    font-size: 1.1rem;
    margin-bottom: 0.75rem;
  }

  .pathway-content p {
    font-size: 0.9rem;
  }
}

/* Reduced motion accessibility */
@media (prefers-reduced-motion: reduce) {
  .achievement-card,
  .pathway-card,
  .pathway-icon,
  .text-center {
    transition: none;
    animation: none;
  }

  .achievement-card,
  .pathway-card,
  .text-center {
    opacity: 1;
    transform: none;
  }
}
</style>
