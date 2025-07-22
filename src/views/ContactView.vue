<template>
  <div class="min-h-screen bg-black text-white">
    <div class="container mx-auto px-6 py-16">
      <!-- Header Section -->
      <div class="text-center mb-16">
        <h1 class="text-5xl font-bold mb-4">Let's Work Together</h1>
        <p class="text-xl text-gray-400 max-w-3xl mx-auto">
          Ready to bring your ideas to life? Let's discuss your project and
          create something amazing together.
        </p>
      </div>

      <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 max-w-6xl mx-auto">
        <!-- Contact Form -->
        <div class="contact-form-container">
          <h2 class="text-3xl font-bold mb-8">Send me a message</h2>
          <form @submit.prevent="submitForm" class="space-y-6">
            <div class="form-group">
              <label for="name" class="form-label">Full Name</label>
              <input
                type="text"
                id="name"
                v-model="form.name"
                class="form-input"
                placeholder="Your full name"
                required
              />
            </div>

            <div class="form-group">
              <label for="email" class="form-label">Email Address</label>
              <input
                type="email"
                id="email"
                v-model="form.email"
                class="form-input"
                placeholder="your.email@example.com"
                required
              />
            </div>

            <div class="form-group">
              <label for="subject" class="form-label">Subject</label>
              <input
                type="text"
                id="subject"
                v-model="form.subject"
                class="form-input"
                placeholder="Project discussion"
                required
              />
            </div>

            <div class="form-group">
              <label for="budget" class="form-label">Project Budget</label>
              <select
                id="budget"
                v-model="form.budget"
                class="form-input"
                required
              >
                <option value="">Select budget range</option>
                <option value="under-5k">Under $5,000</option>
                <option value="5k-10k">$5,000 - $10,000</option>
                <option value="10k-25k">$10,000 - $25,000</option>
                <option value="25k-50k">$25,000 - $50,000</option>
                <option value="50k-plus">$50,000+</option>
              </select>
            </div>

            <div class="form-group">
              <label for="message" class="form-label">Message</label>
              <textarea
                id="message"
                v-model="form.message"
                class="form-input"
                rows="6"
                placeholder="Tell me about your project, goals, and timeline..."
                required
              ></textarea>
            </div>

            <button
              type="submit"
              class="submit-button"
              :disabled="isSubmitting"
            >
              <i class="fas fa-paper-plane mr-2"></i>
              {{ isSubmitting ? "Sending..." : "Send Message" }}
            </button>
          </form>
        </div>

        <!-- Contact Information -->
        <div class="contact-info-container">
          <h2 class="text-3xl font-bold mb-8">Get in touch</h2>

          <div class="space-y-6 mb-8">
            <div class="contact-item">
              <div class="contact-icon">
                <i class="fas fa-envelope"></i>
              </div>
              <div>
                <h3 class="font-semibold">Email</h3>
                <a
                  href="mailto:sok.chanmakara@email.com"
                  class="text-gray-400 hover:text-white transition-colors"
                >
                  sok.chanmakara@email.com
                </a>
              </div>
            </div>

            <div class="contact-item">
              <div class="contact-icon">
                <i class="fas fa-phone"></i>
              </div>
              <div>
                <h3 class="font-semibold">Phone</h3>
                <a
                  href="tel:+855123456789"
                  class="text-gray-400 hover:text-white transition-colors"
                >
                  +855 12 345 6789
                </a>
              </div>
            </div>

            <div class="contact-item">
              <div class="contact-icon">
                <i class="fas fa-map-marker-alt"></i>
              </div>
              <div>
                <h3 class="font-semibold">Location</h3>
                <p class="text-gray-400">Phnom Penh, Cambodia</p>
              </div>
            </div>

            <div class="contact-item">
              <div class="contact-icon">
                <i class="fas fa-clock"></i>
              </div>
              <div>
                <h3 class="font-semibold">Response Time</h3>
                <p class="text-gray-400">Usually within 24 hours</p>
              </div>
            </div>
          </div>

          <!-- Social Links -->
          <div class="social-links">
            <h3 class="text-xl font-bold mb-4">Follow me</h3>
            <div class="flex space-x-4">
              <a href="https://github.com" class="social-link">
                <i class="fab fa-github"></i>
              </a>
              <a href="https://linkedin.com" class="social-link">
                <i class="fab fa-linkedin"></i>
              </a>
              <a href="https://twitter.com" class="social-link">
                <i class="fab fa-twitter"></i>
              </a>
              <a href="https://instagram.com" class="social-link">
                <i class="fab fa-instagram"></i>
              </a>
              <a href="https://facebook.com" class="social-link">
                <i class="fab fa-facebook"></i>
              </a>
            </div>
          </div>

          <!-- Availability Status -->
          <div class="availability-status">
            <div class="status-indicator">
              <div class="status-dot"></div>
              <span class="status-text">Available for new projects</span>
            </div>
            <p class="text-gray-400 text-sm mt-2">
              Currently accepting new freelance projects and collaborations
            </p>
          </div>

          <!-- FAQ -->
          <div class="faq-section">
            <h3 class="text-xl font-bold mb-4">Quick Answers</h3>
            <div class="space-y-3">
              <div class="faq-item">
                <h4 class="font-semibold text-sm">
                  What's your typical project timeline?
                </h4>
                <p class="text-gray-400 text-xs">
                  2-8 weeks depending on complexity
                </p>
              </div>
              <div class="faq-item">
                <h4 class="font-semibold text-sm">Do you work with teams?</h4>
                <p class="text-gray-400 text-xs">
                  Yes, I collaborate with designers and other developers
                </p>
              </div>
              <div class="faq-item">
                <h4 class="font-semibold text-sm">
                  What technologies do you specialize in?
                </h4>
                <p class="text-gray-400 text-xs">
                  Vue.js, React, Node.js, Python, and modern web technologies
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, reactive } from "vue";

const isSubmitting = ref(false);

const form = reactive({
  name: "",
  email: "",
  subject: "",
  budget: "",
  message: "",
});

const submitForm = async () => {
  isSubmitting.value = true;

  try {
    // Simulate form submission
    await new Promise((resolve) => setTimeout(resolve, 2000));

    // Here you would typically send the form data to your backend
    console.log("Form submitted:", form);

    // Reset form
    Object.keys(form).forEach((key) => {
      form[key] = "";
    });

    // Show success message (you can implement a toast notification)
    alert("Thank you for your message! I'll get back to you soon.");
  } catch (error) {
    console.error("Error submitting form:", error);
    alert("There was an error sending your message. Please try again.");
  } finally {
    isSubmitting.value = false;
  }
};
</script>

<style scoped>
.contact-form-container,
.contact-info-container {
  background-color: rgb(17, 24, 39);
  padding: 2rem;
  border-radius: 1rem;
  border: 1px solid rgb(31, 41, 55);
}

.form-group {
  margin-bottom: 1.5rem;
}

.form-label {
  display: block;
  margin-bottom: 0.5rem;
  font-weight: 500;
  color: rgb(209, 213, 219);
}

.form-input {
  width: 100%;
  padding: 0.75rem 1rem;
  background-color: rgb(31, 41, 55);
  border: 1px solid rgb(55, 65, 81);
  border-radius: 0.5rem;
  color: white;
  transition: all 0.3s ease;
}

.form-input:focus {
  outline: none;
  border-color: rgb(99, 102, 241);
  box-shadow: 0 0 0 3px rgba(99, 102, 241, 0.1);
}

.form-input::placeholder {
  color: rgb(107, 114, 128);
}

.submit-button {
  width: 100%;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  padding: 0.75rem 1.5rem;
  border: none;
  border-radius: 0.5rem;
  font-weight: 600;
  transition: all 0.3s ease;
  cursor: pointer;
}

.submit-button:hover:not(:disabled) {
  transform: translateY(-2px);
  box-shadow: 0 10px 25px rgba(102, 126, 234, 0.3);
}

.submit-button:disabled {
  opacity: 0.7;
  cursor: not-allowed;
}

.contact-item {
  display: flex;
  align-items: flex-start;
  gap: 1rem;
}

.contact-icon {
  width: 3rem;
  height: 3rem;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  border-radius: 0.75rem;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  flex-shrink: 0;
}

.social-links {
  margin-top: 2rem;
  padding-top: 2rem;
  border-top: 1px solid rgb(31, 41, 55);
}

.social-link {
  width: 3rem;
  height: 3rem;
  background-color: rgb(31, 41, 55);
  border-radius: 0.75rem;
  display: flex;
  align-items: center;
  justify-content: center;
  color: rgb(156, 163, 175);
  transition: all 0.3s ease;
}

.social-link:hover {
  background-color: rgb(55, 65, 81);
  color: white;
  transform: translateY(-2px);
}

.availability-status {
  margin-top: 2rem;
  padding-top: 2rem;
  border-top: 1px solid rgb(31, 41, 55);
}

.status-indicator {
  display: flex;
  align-items: center;
  gap: 0.75rem;
}

.status-dot {
  width: 0.75rem;
  height: 0.75rem;
  background-color: rgb(34, 197, 94);
  border-radius: 50%;
  animation: pulse 2s infinite;
}

.status-text {
  font-weight: 500;
  color: rgb(34, 197, 94);
}

@keyframes pulse {
  0%,
  100% {
    opacity: 1;
  }
  50% {
    opacity: 0.5;
  }
}

.faq-section {
  margin-top: 2rem;
  padding-top: 2rem;
  border-top: 1px solid rgb(31, 41, 55);
}

.faq-item {
  background-color: rgb(31, 41, 55);
  padding: 1rem;
  border-radius: 0.5rem;
  margin-bottom: 0.75rem;
}

@media (max-width: 768px) {
  .contact-form-container,
  .contact-info-container {
    padding: 1.5rem;
  }
}
</style>
