<template>
  <div class="min-h-screen bg-black text-white">
    <div class="container mx-auto px-6 py-16">
      <!-- Header Section -->
      <div class="text-center mb-16">
        <h1 class="text-5xl font-bold mb-4">Here's Some Of My Work</h1>
        <p class="text-xl text-gray-400 max-w-3xl mx-auto">
          Don't just take my word for it — here's a look at what I've built 🚀
        </p>
      </div>

      <!-- Projects Grid -->
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-12">
        <!-- Project 1 -->
        <div class="project-card">
          <div class="project-image">
            <img
              src="https://images.unsplash.com/photo-1551650975-87deedd944c3?w=600&h=400&fit=crop"
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
              Modern e-commerce solution with real-time inventory management and
              secure payment processing
            </p>
            <div class="project-links">
              <a href="#" class="project-link">
                <i class="fas fa-globe"></i>
                Website
              </a>
              <a href="#" class="project-link">
                <i class="fab fa-github"></i>
                GitHub
              </a>
            </div>
            <div class="tech-stack">
              <span class="tech-tag">Vue.js</span>
              <span class="tech-tag">Node.js</span>
              <span class="tech-tag">MongoDB</span>
              <span class="tech-tag">Stripe</span>
            </div>
          </div>
        </div>

        <!-- Project 2 -->
        <div class="project-card">
          <div class="project-image">
            <img
              src="https://images.unsplash.com/photo-1611224923853-80b023f02d71?w=600&h=400&fit=crop"
              alt="Task Management App"
              class="w-full h-64 object-cover rounded-lg"
            />
          </div>
          <div class="project-content">
            <div class="project-logo">
              <div class="logo-placeholder">TM</div>
            </div>
            <h3 class="text-2xl font-bold mb-3">Task Management App</h3>
            <p class="text-gray-400 mb-4">
              Collaborative task management platform with real-time updates and
              team collaboration features
            </p>
            <div class="project-links">
              <a href="#" class="project-link">
                <i class="fas fa-globe"></i>
                Website
              </a>
              <a href="#" class="project-link">
                <i class="fab fa-github"></i>
                GitHub
              </a>
            </div>
            <div class="tech-stack">
              <span class="tech-tag">React</span>
              <span class="tech-tag">Express</span>
              <span class="tech-tag">Socket.io</span>
              <span class="tech-tag">PostgreSQL</span>
            </div>
          </div>
        </div>

        <!-- Project 3 -->
        <div class="project-card">
          <div class="project-image">
            <img
              src="https://images.unsplash.com/photo-1512486130939-2c4f79935e4f?w=600&h=400&fit=crop"
              alt="Social Media Dashboard"
              class="w-full h-64 object-cover rounded-lg"
            />
          </div>
          <div class="project-content">
            <div class="project-logo">
              <div class="logo-placeholder">SM</div>
            </div>
            <h3 class="text-2xl font-bold mb-3">Social Media Dashboard</h3>
            <p class="text-gray-400 mb-4">
              Analytics dashboard for social media management with data
              visualization and scheduling tools
            </p>
            <div class="project-links">
              <a href="#" class="project-link">
                <i class="fas fa-globe"></i>
                Website
              </a>
              <a href="#" class="project-link">
                <i class="fab fa-github"></i>
                GitHub
              </a>
            </div>
            <div class="tech-stack">
              <span class="tech-tag">Vue.js</span>
              <span class="tech-tag">Python</span>
              <span class="tech-tag">Chart.js</span>
              <span class="tech-tag">Redis</span>
            </div>
          </div>
        </div>

        <!-- Project 4 -->
        <div class="project-card">
          <div class="project-image">
            <img
              src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?w=600&h=400&fit=crop"
              alt="Learning Management System"
              class="w-full h-64 object-cover rounded-lg"
            />
          </div>
          <div class="project-content">
            <div class="project-logo">
              <div class="logo-placeholder">LMS</div>
            </div>
            <h3 class="text-2xl font-bold mb-3">Learning Management System</h3>
            <p class="text-gray-400 mb-4">
              Comprehensive LMS with video streaming, progress tracking, and
              interactive quizzes
            </p>
            <div class="project-links">
              <a href="#" class="project-link">
                <i class="fas fa-globe"></i>
                Website
              </a>
              <a href="#" class="project-link">
                <i class="fab fa-github"></i>
                GitHub
              </a>
            </div>
            <div class="tech-stack">
              <span class="tech-tag">Next.js</span>
              <span class="tech-tag">Django</span>
              <span class="tech-tag">AWS S3</span>
              <span class="tech-tag">MySQL</span>
            </div>
          </div>
        </div>

        <!-- Project 5 -->
        <div class="project-card">
          <div class="project-image">
            <img
              src="https://images.unsplash.com/photo-1563013544-824ae1b704d3?w=600&h=400&fit=crop"
              alt="Real Estate Platform"
              class="w-full h-64 object-cover rounded-lg"
            />
          </div>
          <div class="project-content">
            <div class="project-logo">
              <div class="logo-placeholder">RE</div>
            </div>
            <h3 class="text-2xl font-bold mb-3">Real Estate Platform</h3>
            <p class="text-gray-400 mb-4">
              Property listing platform with advanced search filters and virtual
              tour integration
            </p>
            <div class="project-links">
              <a href="#" class="project-link">
                <i class="fas fa-globe"></i>
                Website
              </a>
              <a href="#" class="project-link">
                <i class="fab fa-github"></i>
                GitHub
              </a>
            </div>
            <div class="tech-stack">
              <span class="tech-tag">React</span>
              <span class="tech-tag">Laravel</span>
              <span class="tech-tag">Maps API</span>
              <span class="tech-tag">MySQL</span>
            </div>
          </div>
        </div>

        <!-- Project 6 -->
        <div class="project-card">
          <div class="project-image">
            <img
              src="https://images.unsplash.com/photo-1586297135537-94bc9ba060aa?w=600&h=400&fit=crop"
              alt="Weather App"
              class="w-full h-64 object-cover rounded-lg"
            />
          </div>
          <div class="project-content">
            <div class="project-logo">
              <div class="logo-placeholder">WA</div>
            </div>
            <h3 class="text-2xl font-bold mb-3">Weather Forecast App</h3>
            <p class="text-gray-400 mb-4">
              Beautiful weather application with detailed forecasts and
              location-based services
            </p>
            <div class="project-links">
              <a href="#" class="project-link">
                <i class="fas fa-globe"></i>
                Website
              </a>
              <a href="#" class="project-link">
                <i class="fab fa-github"></i>
                GitHub
              </a>
            </div>
            <div class="tech-stack">
              <span class="tech-tag">Vue.js</span>
              <span class="tech-tag">Weather API</span>
              <span class="tech-tag">PWA</span>
              <span class="tech-tag">Geolocation</span>
            </div>
          </div>
        </div>
      </div>

      <!-- Call to Action -->
      <div class="text-center mt-16">
        <h2 class="text-3xl font-bold mb-4">Interested in Working Together?</h2>
        <p class="text-gray-400 mb-8">
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
