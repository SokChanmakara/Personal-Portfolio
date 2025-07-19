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
  min-height: 400px;
  border: 1px solid #514f4f;
  border-radius: 30px;
  padding: 20px;
  background-color: var(--color-background);
}

.placeholder {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100%;
  text-align: center;
  color: var(--color-text);
}

.placeholder h2 {
  margin-bottom: 10px;
  color: var(--color-heading);
}

.placeholder p {
  color: var(--color-text);
  opacity: 0.7;
}

@media (max-width: 480px) {
  .main-content {
    padding: 15px;
  }
}
</style>
