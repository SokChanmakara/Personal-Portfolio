<template>
  <div class="about-container">
    <!-- Header Section -->
    <div class="text-center mb-16">
      <h1
        class="text-5xl font-bold mb-10 bg-gradient-to-r from-blue-400 via-purple-500 to-cyan-400 bg-clip-text text-transparent"
      >
        About Me
      </h1>
      <div class="max-w-4xl mx-auto">
        <p class="text-xl text-gray-200 leading-relaxed mb-8 font-medium">
          I'm a Mobile & Web Application developer with 3+ years of experience;
          I develop software using extraordinary abilities, strategy, and design
          to meet any obstacle.
        </p>
        <p class="text-lg text-gray-300 leading-relaxed">
          I have worked on a wide range of projects, from simple apps to complex
          enterprise-level solutions. I am constantly amazed by the power and
          flexibility of Flutter, and I believe that it is the future of mobile
          app development.
        </p>
      </div>
    </div>

    <!-- Milestones & Achievements -->
    <div class="mb-16">
      <h2 class="section-title">🚀 Milestones & Achievements</h2>
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <div class="achievement-card">
          <div
            class="text-6xl font-bold bg-gradient-to-r from-blue-400 to-blue-600 bg-clip-text text-transparent mb-4"
          >
            +3
          </div>
          <div class="text-xl font-bold mb-3 text-white">
            YEARS OF EXPERIENCE
          </div>
          <p class="text-gray-300 leading-relaxed">
            Building innovative solutions across various industries and
            technologies
          </p>
        </div>

        <div class="achievement-card">
          <div
            class="text-6xl font-bold bg-gradient-to-r from-green-400 to-emerald-600 bg-clip-text text-transparent mb-4"
          >
            +15
          </div>
          <div class="text-xl font-bold mb-3 text-white">
            PROJECTS COMPLETED
          </div>
          <p class="text-gray-300 leading-relaxed">
            Successfully delivered applications from concept to production
          </p>
        </div>

        <div class="achievement-card">
          <div
            class="text-6xl font-bold bg-gradient-to-r from-purple-400 to-pink-600 bg-clip-text text-transparent mb-4"
          >
            +7
          </div>
          <div class="text-xl font-bold mb-3 text-white">WORLDWIDE CLIENTS</div>
          <p class="text-gray-300 leading-relaxed">
            Collaborated with clients across different continents and time zones
          </p>
        </div>
      </div>
    </div>

    <!-- Strategic Implementation Pathway -->
    <div class="mb-16">
      <h2
        class="second-section-title"
      >
        Strategic Implementation Pathway
      </h2>
      <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
        <!-- Planning & Strategy -->
        <div class="pathway-card">
          <div class="pathway-icon">
            <i class="fas fa-search text-2xl"></i>
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
            <i class="fas fa-palette text-2xl"></i>
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
            <i class="fas fa-code text-2xl"></i>
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
            <i class="fas fa-rocket text-2xl"></i>
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
import { onMounted } from "vue";

onMounted(() => {
  // Add any animations or interactions here
});
</script>

<style scoped>
.about-container {
  padding: 2rem;
  color: white;
  min-height: 100%;
  overflow-x: hidden;
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
}

.achievement-card {
  background: linear-gradient(
    145deg,
    rgba(99, 102, 241, 0.1) 0%,
    rgba(139, 92, 246, 0.05) 50%,
    rgba(59, 130, 246, 0.1) 100%
  );
  backdrop-filter: blur(10px);
  border: 1px solid rgba(99, 102, 241, 0.2);
  border-radius: 1.5rem;
  padding: 2rem;
  text-align: center;
  transition: all 0.4s ease;
  position: relative;
  overflow: hidden;
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

.achievement-card:hover {
  background: linear-gradient(
    145deg,
    rgba(99, 102, 241, 0.15) 0%,
    rgba(139, 92, 246, 0.1) 50%,
    rgba(59, 130, 246, 0.15) 100%
  );
  border-color: rgba(99, 102, 241, 0.4);
  transform: translateY(-5px) scale(1.02);
  box-shadow: 0 20px 40px rgba(99, 102, 241, 0.2);
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
  padding: 2rem;
  display: flex;
  align-items: flex-start;
  gap: 1.5rem;
  transition: all 0.4s ease;
  position: relative;
  overflow: hidden;
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

.pathway-card:hover {
  background: linear-gradient(
    145deg,
    rgba(255, 255, 255, 0.08) 0%,
    rgba(99, 102, 241, 0.05) 50%,
    rgba(255, 255, 255, 0.03) 100%
  );
  border-color: rgba(99, 102, 241, 0.3);
  transform: translateY(-3px);
  box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
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
  transition: all 0.3s ease;
}

.pathway-card:hover .pathway-icon {
  transform: scale(1.1) rotate(5deg);
  box-shadow: 0 12px 35px rgba(99, 102, 241, 0.4);
}

.pathway-icon.design {
  background: linear-gradient(135deg, #ec4899 0%, #f59e0b 100%);
  box-shadow: 0 8px 25px rgba(236, 72, 153, 0.3);
}

.pathway-card:hover .pathway-icon.design {
  box-shadow: 0 12px 35px rgba(236, 72, 153, 0.4);
}

.pathway-icon.development {
  background: linear-gradient(135deg, #06b6d4 0%, #10b981 100%);
  box-shadow: 0 8px 25px rgba(6, 182, 212, 0.3);
}

.pathway-card:hover .pathway-icon.development {
  box-shadow: 0 12px 35px rgba(6, 182, 212, 0.4);
}

.pathway-icon.launch {
  background: linear-gradient(135deg, #10b981 0%, #84cc16 100%);
  box-shadow: 0 8px 25px rgba(16, 185, 129, 0.3);
}

.pathway-card:hover .pathway-icon.launch {
  box-shadow: 0 12px 35px rgba(16, 185, 129, 0.4);
}

.pathway-content {
  flex: 1;
}

@media (max-width: 768px) {
  .about-container {
    padding: 1rem;
  }

  .pathway-card {
    flex-direction: column;
    text-align: center;
  }

  .pathway-icon {
    margin: 0 auto;
  }
}
</style>
