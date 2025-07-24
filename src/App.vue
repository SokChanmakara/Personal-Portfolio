<script setup>
import { RouterView } from "vue-router";
import { useRoute } from "vue-router";
import ProfileCard from "./components/ProfileCard.vue";
import ContactInfo from "./components/ContactInfo.vue";
import Navbar from "./components/navbar.vue";
import profileImage from "./assets/Image/makara1.png";

const route = useRoute();
</script>

<template>
  <div class="app-container">
    <div class="main-layout">
      <!-- Sidebar - Always visible -->
      <ProfileCard
        name="SOK CHANMAKARA"
        title="SOFTWARE DEVELOPER"
        :profile-image="profileImage"
        alt-text="Profile picture"
      >
        <template #sidebar-content>
          <ContactInfo />

          <!-- Quick Stats -->

          <!-- Download Resume Button -->
        </template>
      </ProfileCard>

      <!-- Main Content Area -->
      <div class="main-content-wrapper">
        <Navbar />
        <div class="content-area">
          <router-view />
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.app-container {
  min-height: 100vh;
  padding: 20px;
}

.main-layout {
  display: flex;
  gap: 20px;
  max-width: 1600px;
  margin: 0 auto;
  flex-wrap: wrap;
}

.main-content-wrapper {
  flex: 1;
  min-height: 600px;
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: 30px;
  background: rgba(255, 255, 255, 0.02);
  backdrop-filter: blur(10px);
  color: #f9fafb;
  overflow: hidden;
}

.content-area {
  height: calc(100% - 80px); /* Subtract navbar height */
  overflow-y: auto;
}

.quick-stats {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1rem;
  margin: 2rem 0;
  padding: 1.5rem;
  background: rgba(255, 255, 255, 0.05);
  border-radius: 1rem;
  border: 1px solid rgba(255, 255, 255, 0.1);
}

.stat-item {
  text-align: center;
}

.stat-number {
  font-size: 1.5rem;
  font-weight: 700;
  color: #64ffda;
  margin-bottom: 0.25rem;
}

.stat-label {
  font-size: 0.75rem;
  color: #8892b0;
  text-transform: uppercase;
  letter-spacing: 0.5px;
}

.resume-download {
  margin-top: 2rem;
}

.download-btn {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 0.5rem;
  width: 100%;
  padding: 1rem;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  text-decoration: none;
  border-radius: 0.75rem;
  font-weight: 600;
  transition: all 0.3s ease;
}

.download-btn:hover {
  transform: translateY(-2px);
  box-shadow: 0 10px 25px rgba(102, 126, 234, 0.3);
}

/* Responsive Design */
@media (max-width: 1200px) {
  .app-container {
    padding: 15px;
  }

  .main-layout {
    max-width: 100%;
  }
}

@media (max-width: 768px) {
  .app-container {
    padding: 10px;
  }

  .main-layout {
    flex-direction: column;
    gap: 15px;
  }

  .quick-stats {
    grid-template-columns: 1fr;
    text-align: center;
  }

  .main-content-wrapper {
    min-height: auto;
  }
}

@media (max-width: 480px) {
  .app-container {
    padding: 5px;
  }

  .main-layout {
    gap: 10px;
  }

  .quick-stats {
    padding: 1rem;
    gap: 0.75rem;
  }

  .stat-number {
    font-size: 1.25rem;
  }

  .stat-label {
    font-size: 0.7rem;
  }
}
</style>
