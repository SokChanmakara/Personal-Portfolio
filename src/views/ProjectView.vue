<template>
  <div class="min-h-screen text-white">
    <div class="container mx-auto px-6 py-16">
      <!-- Projects Grid -->
      <div
        class="grid grid-cols-1 lg:grid-cols-2 gap-12"
        style="margin-top: 16px"
      >
        <!-- Project 1 -->
        <div class="project-card">
          <div class="project-image">
            <img
              src="../assets/Image/rumtum.png"
              alt="E-Commerce Platform"
              class="w-full h-64 object-cover rounded-lg"
            />
          </div>
          <div class="project-content">
            <div class="project-logo">
              <div class="logo-placeholder">EC</div>
            </div>
            <h3 class="text-2xl font-bold mb-3">E-Commerce Platform</h3>
            <p class="text-gray-400 mb-4">
              Modern e-commerce solution with real-time inventory management
              called Rumtum
            </p>
            <div class="project-links">
              <a
                href="https://github.com/SokChanmakara/Rumtum"
                target="_blank"
                rel="noopener"
                class="project-link"
              >
                <font-awesome-icon icon="fa-brands fa-github-alt" />
                GitHub
              </a>
            </div>
            <div class="tech-stack">
              <span class="tech-tag">Vue.js</span>
              <span class="tech-tag">Javascript</span>
              <span class="tech-tag">MySQL</span>
            </div>
          </div>
        </div>

        <!-- Project 2 -->
        <div class="project-card">
          <div class="project-image">
            <img
              src="../assets/Image/bot.png"
              alt="Telegram Bot"
              class="w-full h-64 object-cover rounded-lg"
            />
          </div>
          <div class="project-content">
            <div class="project-logo">
              <div class="logo-placeholder">TB</div>
            </div>
            <h3 class="text-2xl font-bold mb-3">Telegram IT Support Bot</h3>
            <p class="text-gray-400 mb-4">
              A Ticket Bot For IT Support Teams to manage and track support
            </p>
            <div class="project-links">
              <a
                href="https://github.com/SokChanmakara/IT-Support-Bot"
                target="_blank"
                rel="noopener"
                class="project-link"
              >
                <font-awesome-icon icon="fa-brands fa-github-alt" />
                GitHub
              </a>
            </div>
            <div class="tech-stack">
              <span class="tech-tag">Python </span>
            </div>
          </div>
        </div>

        <!-- Project 3 -->
        <div class="project-card">
          <div class="project-image">
            <img
              src="../assets/Image/pteskhmer.png"
              alt="Hotel Booking"
              class="w-full h-64 object-cover rounded-lg"
            />
          </div>
          <div class="project-content">
            <div class="project-logo">
              <div class="logo-placeholder">HB</div>
            </div>
            <h3 class="text-2xl font-bold mb-3">Hotel Booking</h3>
            <p class="text-gray-400 mb-4">Hotel Booking Web Application</p>
            <div class="project-links">
              <a
                href="https://github.com/gitmeas02/Booking_IP"
                target="_blank"
                rel="noopener"
                class="project-link"
              >
                <font-awesome-icon icon="fa-brands fa-github-alt" />
                GitHub
              </a>
            </div>
            <div class="tech-stack">
              <span class="tech-tag">Vue.js</span>
              <span class="tech-tag">Laravel</span>
              <span class="tech-tag">PHP</span>
              <span class="tech-tag">Javascript</span>
              <span class="tech-tag">MySQL</span>
              <span class="tech-tag">MinIO</span>
              <span class="tech-tag">Docker</span>
            </div>
          </div>
        </div>

        <!-- Project 4 -->
        <div class="project-card">
          <div class="project-image">
            <img
              src="../assets/Image/flow.jpg"
              alt="Mobile E-Commerce"
              class="w-full h-64 object-cover rounded-lg"
            />
          </div>
          <div class="project-content">
            <div class="project-logo">
              <div class="logo-placeholder">FW</div>
            </div>
            <h3 class="text-2xl font-bold mb-3">E-Commerce Mobile</h3>
            <p class="text-gray-400 mb-4">
              Flow a mobile E-Commerce application
            </p>
            <div class="project-links">
              <a
                href="https://github.com/gitmeas02/Mobile_App_Flow"
                target="_blank"
                rel="noopener"
                class="project-link"
              >
                <font-awesome-icon icon="fa-brands fa-github-alt" />
                GitHub
              </a>
            </div>
            <div class="tech-stack">
              <span class="tech-tag">Flutter</span>
              <span class="tech-tag">Riverpod</span>
            </div>
          </div>
        </div>

        <!-- Project 5 -->
        <div class="project-card">
          <div class="project-image">
            <img
              src="../assets/Image/demo.gif"
              alt="Crud App"
              class="w-full h-64 object-cover rounded-lg"
            />
          </div>
          <div class="project-content">
            <div class="project-logo">
              <div class="logo-placeholder">CA</div>
            </div>
            <h3 class="text-2xl font-bold mb-3">CRUD APP</h3>
            <p class="text-gray-400 mb-4">Simple CRUD application</p>
            <div class="project-links">
              <a
                href="https://github.com/SokChanmakara/Crud-App?tab=readme-ov-file"
                target="_blank"
                rel="noopener"
                class="project-link"
              >
                <font-awesome-icon icon="fa-brands fa-github-alt" />
                GitHub
              </a>
            </div>
            <div class="tech-stack">
              <span class="tech-tag">Flutter</span>
              <span class="tech-tag">Riverpod</span>
              <span class="tech-tag">ExpressJS</span>
              <span class="tech-tag">Docker</span>
            </div>
          </div>
        </div>
      </div>

      <!-- Project 6 -->

      <!-- Call to Action -->
      <div class="text-center mt-16" style="margin-top: 64px">
        <h2 class="text-3xl font-bold mb-4">Interested in Working Together?</h2>
        <p class="text-gray-400 mb-8" style="margin-bottom: 32px">
          Let's discuss your next project and bring your ideas to life
        </p>
        <router-link
          to="/contact"
          class="inline-block bg-gradient-to-r from-blue-500 to-purple-600 text-white px-8 py-3 rounded-lg font-semibold hover:from-blue-600 hover:to-purple-700 transition-all duration-300"
        >
          Get In Touch
        </router-link>
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
.project-card {
  background-color: rgb(17, 24, 39);
  border-radius: 1rem;
  border: 1px solid rgb(31, 41, 55);
  overflow: hidden;
  transition: all 0.3s ease;
}

.project-card:hover {
  border-color: rgb(75, 85, 99);
  transform: translateY(-0.5rem);
}

.project-content {
  padding: 2rem;
}

.project-logo {
  margin-bottom: 1rem;
}

.logo-placeholder {
  width: 3rem;
  height: 3rem;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  border-radius: 0.5rem;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: bold;
  color: white;
}

.project-links {
  display: flex;
  gap: 1rem;
  margin-top: 1rem;
  margin-bottom: 1rem;
}

.project-link {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  padding: 0.5rem 1rem;
  background-color: rgb(31, 41, 55);
  border-radius: 0.5rem;
  text-decoration: none;
  color: rgb(156, 163, 175);
  transition: all 0.3s ease;
}

.project-link:hover {
  background-color: rgb(55, 65, 81);
  color: white;
}

.tech-stack {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
}

.tech-tag {
  background-color: rgb(55, 65, 81);
  color: rgb(209, 213, 219);
  padding: 0.25rem 0.75rem;
  border-radius: 1rem;
  font-size: 0.75rem;
  font-weight: 500;
}

@media (max-width: 768px) {
  .project-links {
    flex-direction: column;
  }
}
</style>
