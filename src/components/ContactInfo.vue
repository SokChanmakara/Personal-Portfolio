<template>
  <div class="contact-container">
    <div class="contact-item">
      <div class="icon-box">
        <font-awesome-icon :icon="['fas', 'envelope']" class="contact-icon" />
      </div>
      <div class="contact-info">
        <span class="contact-label">EMAIL</span>
        <span class="contact-value">makara@gmail.com</span>
      </div>
    </div>
    <div class="contact-item">
      <div class="icon-box">
        <font-awesome-icon
          :icon="['fas', 'map-marker-alt']"
          class="contact-icon"
        />
      </div>
      <div class="contact-info">
        <span class="contact-label">LOCATION</span>
        <span class="contact-value">Phnom Penh City</span>
      </div>
    </div>
    <div style="display: flex; justify-content: center;">
      <ul class="social-list">
        <li><font-awesome-icon :icon="['fab', 'github']" /></li>
        <li><font-awesome-icon :icon="['fab', 'linkedin']" /></li>
        <li><font-awesome-icon :icon="['fab', 'twitter']" /></li>
        <li><font-awesome-icon :icon="['fab', 'instagram']" /></li>
        <li><font-awesome-icon :icon="['fab', 'google']" /></li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "ContactInfo",
};
</script>

<style scoped>
.contact-container {
  display: flex;
  flex-direction: column;
  gap: 32px;
}

.contact-item {
  display: flex;
  align-items: center;
  gap: 16px;
}

.icon-box {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 48px;
  height: 48px;
  border-radius: 12px;
  background: linear-gradient(45deg, #f0f0f0, #cacaca);
  flex-shrink: 0;
}

.contact-info {
  display: flex;
  flex-direction: column;
  gap: 4px;
}

.contact-label {
  font-size: 12px;
  font-weight: 600;
  color: #666;
  letter-spacing: 0.5px;
}

.contact-value {
  font-size: 14px;
  color: #333;
}

.contact-icon {
  width: 18px;
  height: 18px;
  color: #066666;
}

.social-list {
  display: flex;
  list-style: none;
  padding: 0;
  margin: 0;
  gap: 12px;
  margin-top: 8px;
}

.social-list li {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 32px;
  height: 32px;
  border-radius: 8px;
  background: linear-gradient(45deg, #202020, #1f1d1d);
  cursor: pointer;
  transition: transform 0.2s ease;
}

.social-list li:hover {
  transform: scale(1.1);
}

.social-list svg {
  width: 16px;
  height: 16px;
  color: #ffffff;
}

@media (max-width: 768px) {
  .contact-item {
    gap: 12px;
  }

  .icon-box {
    width: 40px;
    height: 40px;
  }
}
</style>
