<template>
  <nav class="navbar-container">
    <div class="navbar-wrapper">
      <router-link
        to="/"
        class="nav-item home-link"
        exact-active-class="active"
      >
        <i class="fas fa-home"></i>
        <span>Home</span>
      </router-link>
      <router-link
        to="/about"
        class="nav-item"
        active-class="active"
      >
        <i class="fas fa-user"></i>
        <span>About</span>
      </router-link>
      <router-link
        to="/expertise"
        class="nav-item"
        active-class="active"
      >
        <i class="fas fa-code"></i>
        <span>Expertise</span>
      </router-link>
      <router-link
        to="/resume"
        class="nav-item"
        active-class="active"
      >
        <i class="fas fa-file-alt"></i>
        <span>Resume</span>
      </router-link>
      <router-link
        to="/portfolio"
        class="nav-item"
        active-class="active"
      >
        <i class="fas fa-briefcase"></i>
        <span>Portfolio</span>
      </router-link>
      <router-link
        to="/contact"
        class="nav-item"
        active-class="active"
      >
        <i class="fas fa-envelope"></i>
        <span>Contact</span>
      </router-link>
    </div>
  </nav>
</template>

<script setup>
// No additional logic needed for now
</script>

<style scoped>
.navbar-container {
  display: flex;
  justify-content: center;
  padding: 1rem;
  position: sticky;
  top: 0;
  z-index: 100;
  backdrop-filter: blur(20px);
}

.navbar-wrapper {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  padding: 0.75rem 1.5rem;
  background: linear-gradient(
    145deg,
    rgba(26, 32, 56, 0.9) 0%,
    rgba(17, 24, 39, 0.95) 50%,
    rgba(15, 23, 42, 0.9) 100%
  );
  backdrop-filter: blur(20px);
  border: 1px solid rgba(99, 102, 241, 0.2);
  border-radius: 2rem;
  box-shadow: 
    0 20px 40px rgba(0, 0, 0, 0.3),
    0 0 20px rgba(99, 102, 241, 0.1),
    inset 0 1px 0 rgba(255, 255, 255, 0.1);
  transition: all 0.3s ease;
}

.navbar-wrapper:hover {
  border-color: rgba(99, 102, 241, 0.4);
  box-shadow: 
    0 25px 50px rgba(0, 0, 0, 0.4),
    0 0 30px rgba(99, 102, 241, 0.2),
    inset 0 1px 0 rgba(255, 255, 255, 0.15);
  transform: translateY(-2px);
}

.nav-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 0.25rem;
  padding: 0.75rem 1rem;
  border-radius: 1rem;
  color: rgba(156, 163, 175, 0.8);
  text-decoration: none;
  font-weight: 500;
  font-size: 0.875rem;
  transition: all 0.3s ease;
  position: relative;
  min-width: 4rem;
  overflow: hidden;
}

.nav-item i {
  font-size: 1.2rem;
  margin-bottom: 0.25rem;
  transition: all 0.3s ease;
}

.nav-item span {
  font-size: 0.75rem;
  letter-spacing: 0.5px;
  transition: all 0.3s ease;
}

.nav-item:hover {
  color: #ffffff;
  background: linear-gradient(
    135deg,
    rgba(99, 102, 241, 0.2) 0%,
    rgba(139, 92, 246, 0.2) 100%
  );
  transform: translateY(-2px);
  box-shadow: 0 8px 25px rgba(99, 102, 241, 0.3);
}

.nav-item:hover i {
  transform: scale(1.1);
  color: #64ffda;
}

.nav-item.active {
  color: #ffffff;
  background: linear-gradient(
    135deg,
    rgba(99, 102, 241, 0.3) 0%,
    rgba(139, 92, 246, 0.3) 100%
  );
  box-shadow: 
    0 8px 20px rgba(99, 102, 241, 0.4),
    inset 0 1px 0 rgba(255, 255, 255, 0.2);
}

.nav-item.active i {
  color: #64ffda;
  transform: scale(1.1);
}

.nav-item.active::before {
  content: '';
  position: absolute;
  bottom: 0;
  left: 50%;
  transform: translateX(-50%);
  width: 20px;
  height: 2px;
  background: linear-gradient(90deg, #6366f1, #8b5cf6);
  border-radius: 2px;
  animation: glow 2s ease-in-out infinite alternate;
}

@keyframes glow {
  from {
    box-shadow: 0 0 5px #6366f1;
  }
  to {
    box-shadow: 0 0 15px #8b5cf6;
  }
}

.home-link {
  margin-right: 0.5rem;
  border-right: 1px solid rgba(99, 102, 241, 0.2);
  padding-right: 1.5rem;
}

/* Responsive Design */
@media (max-width: 768px) {
  .navbar-wrapper {
    gap: 0.25rem;
    padding: 0.5rem 1rem;
  }
  
  .nav-item {
    padding: 0.5rem 0.75rem;
    min-width: 3rem;
  }
  
  .nav-item span {
    font-size: 0.7rem;
  }
  
  .nav-item i {
    font-size: 1rem;
  }
  
  .home-link {
    margin-right: 0.25rem;
    padding-right: 1rem;
  }
}

@media (max-width: 640px) {
  .nav-item span {
    display: none;
  }
  
  .nav-item {
    min-width: 2.5rem;
    padding: 0.75rem 0.5rem;
  }
  
  .nav-item i {
    margin-bottom: 0;
  }
}
</style>
