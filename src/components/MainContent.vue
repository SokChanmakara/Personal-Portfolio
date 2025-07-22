<script setup>
defineProps({
  title: {
    type: String,
    default: "Main Content",
  },
});
</script>

<template>
  <div class="main-content">
    <slot>
      <!-- Default content if no slot content is provided -->
      <div class="placeholder">
        <h2>{{ title }}</h2>
        <p>Main Content Area.</p>
      </div>
    </slot>
  </div>
</template>

<style scoped>
.main-content {
  flex: 1;
  min-height: 600px;
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: 30px;
  background: rgba(255, 255, 255, 0.02);
  backdrop-filter: blur(10px);
  color: #f9fafb;
  padding: 0;
  overflow: hidden;
}

.placeholder {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100%;
  text-align: center;
  color: #d1d5db;
  padding: 2rem;
}

.placeholder h2 {
  margin-bottom: 10px;
  color: #f9fafb;
}

.placeholder p {
  color: #9ca3af;
  opacity: 0.8;
}

@media (max-width: 768px) {
  .main-content {
    min-height: 500px;
  }
}

@media (max-width: 480px) {
  .main-content {
    min-height: 400px;
    padding: 0;
  }
}
</style>
