<script setup>
defineProps({
  name: {
    type: String,
    default: "SOK CHANMAKARA",
  },
  title: {
    type: String,
    default: "SOFTWARE DEVELOPER",
  },
  profileImage: {
    type: String,
    default:
      "https://i.pinimg.com/736x/cf/d1/df/cfd1df905cde736fc5bf7704de635d7b.jpg",
  },
  altText: {
    type: String,
    default: "Profile picture",
  },
});
</script>

<template>
  <div class="sidebar">
    <div class="profile">
      <div class="image">
        <img :src="profileImage" :alt="altText" />
      </div>
      <div class="name-container">
        <div class="name">
          <p>{{ name }}</p>
        </div>
        <div class="title">
          <p>{{ title }}</p>
        </div>
      </div>
    </div>
    <div class="sidebar-info">
      <slot name="sidebar-content" />
    </div>
  </div>
</template>

<style scoped>
.sidebar {
  width: 100%;
  height: fit-content;
  max-height: calc(100vh - 40px);
  max-width: 350px;
  min-width: 280px;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  padding: 30px 25px;
  background: linear-gradient(
    145deg,
    rgba(26, 32, 56, 0.95) 0%,
    rgba(17, 24, 39, 0.98) 50%,
    rgba(15, 23, 42, 0.95) 100%
  );
  backdrop-filter: blur(20px);
  border: 1px solid rgba(99, 102, 241, 0.2);
  border-radius: 25px;
  box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3),
    inset 0 1px 0 rgba(255, 255, 255, 0.1);
  flex: 0 0 auto;
  position: sticky;
  top: 20px;
  overflow-y: auto;
  transition: all 0.3s ease;
}

.sidebar:hover {
  border-color: rgba(99, 102, 241, 0.4);
  box-shadow: 0 25px 80px rgba(0, 0, 0, 0.4), 0 0 30px rgba(99, 102, 241, 0.1),
    inset 0 1px 0 rgba(255, 255, 255, 0.15);
  transform: translateY(-2px);
}

.profile {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  width: 100%;
  margin-bottom: 25px;
}

.name-container {
  padding: 25px 0;
}

.name p {
  font-size: 1.4rem;
  font-weight: 700;
  background: linear-gradient(135deg, #ffffff 0%, #e2e8f0 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  margin: 0 0 12px 0;
  letter-spacing: 0.5px;
}

.title {
  font-size: 0.85rem;
  position: relative;
  margin-bottom: 30px;
}

.title::after {
  content: "";
  position: absolute;
  bottom: -20px;
  left: 50%;
  transform: translateX(-50%);
  width: 80%;
  height: 2px;
  background: linear-gradient(
    90deg,
    transparent 0%,
    #6366f1 20%,
    #8b5cf6 50%,
    #6366f1 80%,
    transparent 100%
  );
  border-radius: 2px;
  animation: shimmer 3s ease-in-out infinite;
}

@keyframes shimmer {
  0%,
  100% {
    opacity: 0.6;
  }
  50% {
    opacity: 1;
  }
}

.title p {
  margin: 0;
  padding: 8px 16px;
  border-radius: 20px;
  color: #e2e8f0;
  background: linear-gradient(
    135deg,
    rgba(99, 102, 241, 0.8) 0%,
    rgba(139, 92, 246, 0.8) 100%
  );
  font-weight: 500;
  letter-spacing: 1px;
  text-transform: uppercase;
  font-size: 0.75rem;
  box-shadow: 0 4px 15px rgba(99, 102, 241, 0.3);
}

.image {
  margin-bottom: 20px;
  position: relative;
}

.image::before {
  content: "";
  position: absolute;
  top: -8px;
  left: -8px;
  right: -8px;
  bottom: -8px;
  background: linear-gradient(135deg, #6366f1, #8b5cf6, #ec4899);
  border-radius: 28px;
  z-index: -1;
  animation: rotate 6s linear infinite;
}

@keyframes rotate {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(360deg);
  }
}

.image img {
  height: 160px;
  width: 160px;
  border-radius: 20px;
  object-fit: cover;
  border: 3px solid rgba(255, 255, 255, 0.1);
  transition: all 0.3s ease;
}

.image:hover img {
  transform: scale(1.05);
  border-color: rgba(255, 255, 255, 0.2);
}

.sidebar-info {
  flex: 1;
  overflow-y: auto;
}

/* Custom scrollbar for sidebar content */
.sidebar-info::-webkit-scrollbar {
  width: 6px;
}

.sidebar-info::-webkit-scrollbar-track {
  background: rgba(255, 255, 255, 0.05);
  border-radius: 3px;
}

.sidebar-info::-webkit-scrollbar-thumb {
  background: linear-gradient(135deg, #6366f1, #8b5cf6);
  border-radius: 3px;
}

.sidebar-info::-webkit-scrollbar-thumb:hover {
  background: linear-gradient(135deg, #5855eb, #7c3aed);
}

/* Responsive breakpoints */
@media (max-width: 1200px) {
  .sidebar {
    max-width: 320px;
    min-width: 260px;
  }
}

@media (max-width: 1024px) {
  .sidebar {
    position: relative;
    top: auto;
    max-height: none;
    max-width: 300px;
    min-width: 240px;
  }
}

@media (max-width: 768px) {
  .sidebar {
    max-width: 100%;
    min-width: 100%;
    margin: 0 auto;
    position: relative;
    top: auto;
    padding: 25px 20px;
  }

  .image img {
    height: 140px;
    width: 140px;
  }

  .name p {
    font-size: 1.2rem;
  }

  .name-container {
    padding: 20px 0;
  }

  .title p {
    font-size: 0.75rem;
    padding: 8px 16px;
  }
}

@media (max-width: 480px) {
  .sidebar {
    padding: 25px 20px;
  }

  .name-container {
    padding: 20px 0;
  }

  .image img {
    height: 120px;
    width: 120px;
  }

  .name p {
    font-size: 1.1rem;
  }

  .title p {
    font-size: 0.7rem;
    padding: 6px 12px;
  }
}
</style>
