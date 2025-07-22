<template>
  <div class="contact-container">
    <div class="contact-item">
      <div class="icon-box">
        <font-awesome-icon :icon="['fas', 'envelope']" class="contact-icon" />
      </div>
      <div class="contact-info">
        <span class="contact-label">EMAIL</span>
        <span class="contact-value">sokchanmakara04@gmail.com</span>
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
        <span class="contact-value">Phnom Penh City, Cambodia</span>
      </div>
    </div>
    <div class="social-container">
      <ul class="social-list">
        <li>
          <a
            href="https://github.com/SokChanmakara"
            target="_blank"
            rel="noopener"
          >
            <font-awesome-icon :icon="['fab', 'github']" />
          </a>
        </li>
        <li>
          <a
            href="https://www.linkedin.com/in/sok-chanmakara-3a6300307/"
            target="_blank"
            rel="noopener"
          >
            <font-awesome-icon :icon="['fab', 'linkedin']" />
          </a>
        </li>
        <li>
          <a href="https://t.me/Chanmakaraaa" target="_blank" rel="noopener">
            <font-awesome-icon icon="fa-brands fa-telegram" />
          </a>
        </li>
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
  gap: 24px;
  overflow: hidden;
}

.contact-item {
  display: flex;
  align-items: center;
  gap: 16px;
  padding: 16px;
  background: rgba(255, 255, 255, 0.03);
  border-radius: 15px;
  border: 1px solid rgba(99, 102, 241, 0.1);
  transition: all 0.3s ease;
}

.contact-item:hover {
  background: rgba(255, 255, 255, 0.05);
  border-color: rgba(99, 102, 241, 0.3);
  transform: translateY(-2px);
  box-shadow: 0 8px 25px rgba(99, 102, 241, 0.2);
}

.icon-box {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 48px;
  height: 48px;
  border-radius: 12px;
  background: linear-gradient(135deg, #6366f1 0%, #8b5cf6 100%);
  flex-shrink: 0;
  box-shadow: 0 8px 25px rgba(99, 102, 241, 0.3);
}

.contact-info {
  display: flex;
  flex-direction: column;
  gap: 4px;
}

.contact-label {
  font-size: 11px;
  font-weight: 600;
  color: #9ca3af;
  letter-spacing: 1px;
  text-transform: uppercase;
}

.contact-value {
  font-size: 14px;
  color: #e5e7eb;
  font-weight: 500;
}

.contact-icon {
  width: 18px;
  height: 18px;
  color: white;
}

.social-container {
  display: flex;
  justify-content: center;
  overflow: hidden;
  padding: 0 10px;
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
  width: 40px;
  height: 40px;
  border-radius: 12px;
  background: linear-gradient(
    135deg,
    rgba(99, 102, 241, 0.1) 0%,
    rgba(139, 92, 246, 0.1) 100%
  );
  border: 1px solid rgba(99, 102, 241, 0.2);
  cursor: pointer;
  transition: all 0.3s ease;
}

.social-list li:hover {
  background: linear-gradient(135deg, #6366f1 0%, #8b5cf6 100%);
  border-color: rgba(99, 102, 241, 0.5);
  transform: translateY(-3px);
  box-shadow: 0 8px 25px rgba(99, 102, 241, 0.4);
}

.social-list svg {
  width: 18px;
  height: 18px;
  color: #9ca3af;
  transition: color 0.3s ease;
}

.social-list li:hover svg {
  color: white;
}

@media (max-width: 768px) {
  .contact-item {
    gap: 12px;
    padding: 12px;
  }

  .icon-box {
    width: 40px;
    height: 40px;
  }

  .social-list li {
    width: 36px;
    height: 36px;
  }

  .social-list svg {
    width: 16px;
    height: 16px;
  }
}
</style>
