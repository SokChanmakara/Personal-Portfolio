<template>
  <div
    class="min-h-screen  text-white relative overflow-hidden"
  >


    <div class="container mx-auto px-6 py-16 relative z-10">
      <!-- Header Section -->
      <div class="text-center mb-16 header-section">
        <h1
          class="text-6xl font-bold mb-6 bg-gradient-to-r from-blue-400 via-purple-500 to-emerald-400 bg-clip-text text-transparent animate-fade-in"
        >
          Contact For Work
        </h1>
        <p
          class="text-xl text-gray-300 max-w-3xl mx-auto leading-relaxed animate-slide-up"
        >
          Currently, Open for work. 
          Let's discuss your project and
          create something amazing together.
        </p>
      </div>

      <div class=" grid-cols-1 lg:grid-cols-2 gap-12 max-w-7xl mx-auto flex justify-center">
        <!-- Contact Form -->
        <div class="contact-form-container animate-slide-left">
          <div class="flex items-center mb-8">
            <h2
              class="text-3xl font-bold bg-gradient-to-r from-blue-400 to-purple-400 bg-clip-text text-transparent"
            >
              Send me a message
            </h2>
          </div>
          <form @submit.prevent="submitForm" class="space-y-6">
            <div class="form-group">
              <label for="name" class="form-label">
                Full Name
                <span class="text-red-400 ml-1">*</span>
              </label>
              <div class="relative">
                <input
                  type="text"
                  id="name"
                  v-model="form.name"
                  class="form-input"
                  :class="{
                    'border-red-500': errors.name,
                    'border-green-500': form.name && !errors.name,
                  }"
                  placeholder="Your full name"
                  required
                  @blur="validateField('name')"
                  @input="clearError('name')"
                />
                <div
                  class="absolute right-3 top-1/2 transform -translate-y-1/2"
                >
                  <i
                    v-if="form.name && !errors.name"
                    class="fas fa-check text-green-500 text-sm"
                  ></i>
                  <i
                    v-if="errors.name"
                    class="fas fa-exclamation-circle text-red-500 text-sm"
                  ></i>
                </div>
              </div>
              <div v-if="errors.name" class="error-message">
                <i class="fas fa-exclamation-triangle mr-2"></i>
                {{ errors.name }}
              </div>
            </div>

            <div class="form-group">
              <label for="email" class="form-label">
                Email Address
                <span class="text-red-400 ml-1">*</span>
              </label>
              <div class="relative">
                <input
                  type="email"
                  id="email"
                  v-model="form.email"
                  class="form-input"
                  :class="{
                    'border-red-500': errors.email,
                    'border-green-500': form.email && !errors.email,
                  }"
                  placeholder="your.email@example.com"
                  required
                  @blur="validateField('email')"
                  @input="clearError('email')"
                />
                <div
                  class="absolute right-3 top-1/2 transform -translate-y-1/2"
                >
                  <i
                    v-if="form.email && !errors.email"
                    class="fas fa-check text-green-500 text-sm"
                  ></i>
                  <i
                    v-if="errors.email"
                    class="fas fa-exclamation-circle text-red-500 text-sm"
                  ></i>
                </div>
              </div>
              <div v-if="errors.email" class="error-message">
                <i class="fas fa-exclamation-triangle mr-2"></i>
                {{ errors.email }}
              </div>
            </div>

            <div class="form-group">
              <label for="subject" class="form-label">
                Subject
                <span class="text-red-400 ml-1">*</span>
              </label>
              <div class="relative">
                <input
                  type="text"
                  id="subject"
                  v-model="form.subject"
                  class="form-input"
                  :class="{
                    'border-red-500': errors.subject,
                    'border-green-500': form.subject && !errors.subject,
                  }"
                  placeholder="Project discussion"
                  required
                  @blur="validateField('subject')"
                  @input="clearError('subject')"
                />
                <div
                  class="absolute right-3 top-1/2 transform -translate-y-1/2"
                >
                  <i
                    v-if="form.subject && !errors.subject"
                    class="fas fa-check text-green-500 text-sm"
                  ></i>
                  <i
                    v-if="errors.subject"
                    class="fas fa-exclamation-circle text-red-500 text-sm"
                  ></i>
                </div>
              </div>
              <div v-if="errors.subject" class="error-message">
                <i class="fas fa-exclamation-triangle mr-2"></i>
                {{ errors.subject }}
              </div>
            </div>

            <div class="form-group">
              <label for="message" class="form-label">
                Message
                <span class="text-red-400 ml-1">*</span>
              </label>
              <div class="relative">
                <textarea
                  id="message"
                  v-model="form.message"
                  class="form-input resize-none"
                  :class="{
                    'border-red-500': errors.message,
                    'border-green-500': form.message && !errors.message,
                  }"
                  rows="6"
                  placeholder="Tell me about your project, goals, and timeline..."
                  required
                  @blur="validateField('message')"
                  @input="clearError('message')"
                ></textarea>
                <div class="absolute right-3 top-4">
                  <i
                    v-if="form.message && !errors.message"
                    class="fas fa-check text-green-500 text-sm"
                  ></i>
                  <i
                    v-if="errors.message"
                    class="fas fa-exclamation-circle text-red-500 text-sm"
                  ></i>
                </div>
                <div class="absolute bottom-3 right-3 text-xs text-gray-400">
                  {{ form.message.length }}/500
                </div>
              </div>
              <div v-if="errors.message" class="error-message">
                <i class="fas fa-exclamation-triangle mr-2"></i>
                {{ errors.message }}
              </div>
            </div>

            <button
              type="submit"
              class="submit-button group"
              :disabled="isSubmitting || !isFormValid"
              :class="{ 'opacity-50 cursor-not-allowed': !isFormValid }"
              :title="
                isFormValid
                  ? 'Press Ctrl+Enter to submit quickly'
                  : 'Please fill all required fields'
              "
            >
              <span class="flex items-center justify-center">
                <div v-if="isSubmitting" class="loading-spinner mr-2"></div>
                <i
                  v-else
                  class="fas fa-paper-plane mr-2 transition-transform group-hover:translate-x-1"
                ></i>
                {{ isSubmitting ? "Sending..." : "Send Message" }}
              </span>
              <div class="button-glow"></div>
            </button>

            <div class="text-center" style="margin-top: 12px">
              <p class="text-xs text-gray-400">
                <i class="fas fa-keyboard mr-1"></i>
                Tip: Press <kbd class="kbd">Ctrl+Enter</kbd> to submit quickly
              </p>
            </div>
          </form>

          <!-- Quick Answers Section -->
          <div
            class="quick-answers-section mt-8 mb-8 pt-8 border-t border-gray-700/50"
          >
            <h3
              class="text-xl font-semibold text-white mb-16 flex items-center"
            >
              <i class="fas fa-lightning-bolt text-yellow-400 mr-2"></i>
              Quick Answers
            </h3>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-3 " style="margin-top: 12px;">
              <button
                v-for="answer in quickAnswers"
                :key="answer.id"
                @click="selectQuickAnswer(answer)"
                class="quick-answer-btn text-left p-3 rounded-lg bg-slate-700/50 hover:bg-slate-600/50 border border-slate-600/50 hover:border-blue-400/50 transition-all duration-300 group"
              >
                <div class="flex items-start gap-3">
                  <i
                    :class="answer.icon"
                    class="text-blue-400 mt-1 group-hover:scale-110 transition-transform"
                  ></i>
                  <div>
                    <h4 class="font-medium text-white text-sm">
                      {{ answer.title }}
                    </h4>
                    <p class="text-gray-400 text-xs mt-1">
                      {{ answer.preview }}
                    </p>
                  </div>
                </div>
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Toast Notifications -->
    <div
      v-if="showSuccessToast"
      class="fixed top-6 right-6 z-50 bg-gradient-to-r from-green-500 to-emerald-600 text-white px-6 py-4 rounded-xl shadow-2xl border border-green-400/30 backdrop-blur-lg animate-slide-in-right"
    >
      <div class="flex items-center">
        <i class="fas fa-check-circle text-xl mr-3"></i>
        <div>
          <h4 class="font-semibold">Success!</h4>
          <p class="text-sm opacity-90">{{ toastMessage }}</p>
        </div>
        <button
          @click="showSuccessToast = false"
          class="ml-4 text-white/70 hover:text-white transition-colors"
        >
          <i class="fas fa-times"></i>
        </button>
      </div>
    </div>

    <div
      v-if="showErrorToast"
      class="fixed top-6 right-6 z-50 bg-gradient-to-r from-red-500 to-rose-600 text-white px-6 py-4 rounded-xl shadow-2xl border border-red-400/30 backdrop-blur-lg animate-slide-in-right"
    >
      <div class="flex items-center">
        <i class="fas fa-exclamation-circle text-xl mr-3"></i>
        <div>
          <h4 class="font-semibold">Error!</h4>
          <p class="text-sm opacity-90">{{ toastMessage }}</p>
        </div>
        <button
          @click="showErrorToast = false"
          class="ml-4 text-white/70 hover:text-white transition-colors"
        >
          <i class="fas fa-times"></i>
        </button>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, reactive, onMounted, computed, watch } from "vue";

const isSubmitting = ref(false);
const showSuccessToast = ref(false);
const showErrorToast = ref(false);
const toastMessage = ref("");

const form = reactive({
  name: "",
  email: "",
  subject: "",
  budget: "",
  message: "",
});

const errors = reactive({
  name: "",
  email: "",
  subject: "",
  message: "",
});

// Quick answers data
const quickAnswers = ref([
  {
    id: 1,
    title: "Project Consultation",
    preview: "Discuss project requirements and timeline",
    icon: "fas fa-lightbulb",
    subject: "Project Consultation Request",
    message:
      "Hi! I'd like to discuss a new project with you. Could we schedule a consultation to go over the requirements and timeline? I'm particularly interested in [describe your project type].",
  },
  {
    id: 2,
    title: "General Inquiry",
    preview: "Ask about services and availability",
    icon: "fas fa-info-circle",
    subject: "General Inquiry",
    message:
      "Hello! I'm interested in learning more about your services and current availability. Could you provide more information about how you work and your rates?",
  },
  {
    id: 3,
    title: "Technical Question",
    preview: "Get help with technical challenges",
    icon: "fas fa-code",
    subject: "Technical Question",
    message:
      "Hi! I have a technical question about [technology/framework]. I'm currently working on [brief description] and would appreciate your expertise on this matter.",
  },
  {
    id: 4,
    title: "Collaboration",
    preview: "Explore partnership opportunities",
    icon: "fas fa-handshake",
    subject: "Collaboration Opportunity",
    message:
      "Hello! I'm reaching out to explore potential collaboration opportunities. I believe our skills could complement each other well for [type of projects].",
  },
  {
    id: 5,
    title: "Urgent Support",
    preview: "Request immediate assistance",
    icon: "fas fa-exclamation-triangle",
    subject: "Urgent Support Needed",
    message:
      "Hi! I need urgent assistance with [brief description of the issue]. This is time-sensitive and I would greatly appreciate your quick response.",
  },
  {
    id: 6,
    title: "Just Say Hi",
    preview: "Start a friendly conversation",
    icon: "fas fa-smile",
    subject: "Hello!",
    message:
      "Hi! I came across your portfolio and wanted to say hello. Your work is impressive! I'd love to connect and learn more about your journey in development.",
  },
]);

// Validation rules
const validationRules = {
  name: {
    required: true,
    minLength: 2,
    pattern: /^[a-zA-Z\s]+$/,
  },
  email: {
    required: true,
    pattern: /^[^\s@]+@[^\s@]+\.[^\s@]+$/,
  },
  subject: {
    required: true,
    minLength: 3,
  },
  message: {
    required: true,
    minLength: 10,
    maxLength: 500,
  },
};

// Computed property to check if form is valid
const isFormValid = computed(() => {
  return (
    form.name &&
    form.email &&
    form.subject &&
    form.message &&
    !errors.name &&
    !errors.email &&
    !errors.subject &&
    !errors.message
  );
});

// Watch message length to prevent exceeding limit
watch(
  () => form.message,
  (newValue) => {
    if (newValue.length > 500) {
      form.message = newValue.substring(0, 500);
    }
  }
);

// Validation functions
const validateField = (fieldName) => {
  const value = form[fieldName];
  const rules = validationRules[fieldName];

  if (!rules) return;

  // Clear previous error
  errors[fieldName] = "";

  // Required validation
  if (rules.required && (!value || value.trim() === "")) {
    errors[fieldName] = `${
      fieldName.charAt(0).toUpperCase() + fieldName.slice(1)
    } is required`;
    return;
  }

  // Skip other validations if field is empty and not required
  if (!value) return;

  // Min length validation
  if (rules.minLength && value.length < rules.minLength) {
    errors[fieldName] = `${
      fieldName.charAt(0).toUpperCase() + fieldName.slice(1)
    } must be at least ${rules.minLength} characters`;
    return;
  }

  // Max length validation
  if (rules.maxLength && value.length > rules.maxLength) {
    errors[fieldName] = `${
      fieldName.charAt(0).toUpperCase() + fieldName.slice(1)
    } must not exceed ${rules.maxLength} characters`;
    return;
  }

  // Pattern validation
  if (rules.pattern && !rules.pattern.test(value)) {
    switch (fieldName) {
      case "name":
        errors[fieldName] = "Name should only contain letters and spaces";
        break;
      case "email":
        errors[fieldName] = "Please enter a valid email address";
        break;
      default:
        errors[fieldName] = `Invalid ${fieldName} format`;
    }
  }
};

const clearError = (fieldName) => {
  errors[fieldName] = "";
};

const selectQuickAnswer = (answer) => {
  form.subject = answer.subject;
  form.message = answer.message;

  // Clear any existing errors for these fields
  clearError("subject");
  clearError("message");

  // Show a subtle indication that the template was applied
  showToast(
    "Quick answer template applied! Feel free to customize the message.",
    "success"
  );

  // Focus on the name field if empty, otherwise focus on message for customization
  setTimeout(() => {
    if (!form.name) {
      document.getElementById("name")?.focus();
    } else {
      document.getElementById("message")?.focus();
      // Move cursor to end of message for easy editing
      const messageField = document.getElementById("message");
      if (messageField) {
        messageField.setSelectionRange(
          messageField.value.length,
          messageField.value.length
        );
      }
    }
  }, 100);
};

const validateForm = () => {
  Object.keys(validationRules).forEach(validateField);
  return Object.values(errors).every((error) => !error);
};

const showToast = (message, type = "success") => {
  toastMessage.value = message;
  if (type === "success") {
    showSuccessToast.value = true;
    setTimeout(() => {
      showSuccessToast.value = false;
    }, 5000);
  } else {
    showErrorToast.value = true;
    setTimeout(() => {
      showErrorToast.value = false;
    }, 5000);
  }
};

const resetForm = () => {
  Object.keys(form).forEach((key) => {
    form[key] = "";
  });
  Object.keys(errors).forEach((key) => {
    errors[key] = "";
  });
};

onMounted(() => {
  // Add intersection observer for animations
  const observer = new IntersectionObserver(
    (entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.add("animate-in");
        }
      });
    },
    {
      threshold: 0.1,
      rootMargin: "0px 0px -50px 0px",
    }
  );

  // Observe animated elements
  const animatedElements = document.querySelectorAll(
    ".header-section, .contact-form-container, .contact-info-container, .contact-item, .faq-item"
  );

  animatedElements.forEach((element) => {
    observer.observe(element);
  });

  // Add keyboard shortcuts
  const handleKeyboard = (event) => {
    // Escape to close toasts
    if (event.key === "Escape") {
      showSuccessToast.value = false;
      showErrorToast.value = false;
    }

    // Ctrl/Cmd + Enter to submit form
    if ((event.ctrlKey || event.metaKey) && event.key === "Enter") {
      event.preventDefault();
      if (isFormValid.value && !isSubmitting.value) {
        submitForm();
      }
    }
  };

  document.addEventListener("keydown", handleKeyboard);

  // Cleanup
  return () => {
    document.removeEventListener("keydown", handleKeyboard);
  };
});

const submitForm = async () => {
  // Validate form before submission
  if (!validateForm()) {
    showToast("Please fix the errors in the form", "error");
    // Focus on first error field
    const firstErrorField = Object.keys(errors).find((key) => errors[key]);
    if (firstErrorField) {
      const element = document.getElementById(firstErrorField);
      element?.focus();
    }
    return;
  }

  isSubmitting.value = true;

  try {
    // Simulate form submission with more realistic delay
    await new Promise((resolve) => setTimeout(resolve, 2000));

    // Here you would typically send the form data to your backend
    console.log("Form submitted:", form);

    // Reset form
    resetForm();

    // Show success message
    showToast(
      "Thank you for your message! I'll get back to you within 24 hours."
    );

    // Focus back to name field for potential new submission
    setTimeout(() => {
      document.getElementById("name")?.focus();
    }, 100);
  } catch (error) {
    console.error("Error submitting form:", error);
    showToast(
      "There was an error sending your message. Please try again.",
      "error"
    );
  } finally {
    isSubmitting.value = false;
  }
};
</script>

<style scoped>
/* Header Animations */
.header-section {
  opacity: 0;
  transform: translateY(30px);
  animation: fadeInUp 1s ease-out 0.3s forwards;
}

@keyframes fadeInUp {
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes slideInLeft {
  from {
    opacity: 0;
    transform: translateX(-50px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes slideInRight {
  from {
    opacity: 0;
    transform: translateX(50px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes slideInRight {
  from {
    opacity: 0;
    transform: translateX(100px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes spin {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}

@keyframes expand {
  from {
    width: 0;
  }
  to {
    width: 6rem;
  }
}

.animate-slide-in-right {
  animation: slideInRight 0.5s ease-out forwards;
}

.animate-fade-in {
  animation: fadeInUp 1s ease-out forwards;
}

.animate-slide-up {
  animation: fadeInUp 1s ease-out 0.5s forwards;
  opacity: 0;
}

.animate-expand {
  animation: expand 1.5s ease-out 1s forwards;
  width: 0;
}

.animate-slide-left {
  animation: slideInLeft 0.8s ease-out 0.7s forwards;
  opacity: 0;
}

.animate-slide-right {
  animation: slideInRight 0.8s ease-out 0.8s forwards;
  opacity: 0;
}

/* Loading spinner */
.loading-spinner {
  width: 1rem;
  height: 1rem;
  border: 2px solid rgba(255, 255, 255, 0.3);
  border-top: 2px solid white;
  border-radius: 50%;
  animation: spin 1s linear infinite;
}

/* Error message styles */
.error-message {
  margin-top: 0.5rem;
  padding: 0.5rem 0.75rem;
  background: linear-gradient(
    135deg,
    rgba(239, 68, 68, 0.1),
    rgba(220, 38, 38, 0.1)
  );
  border: 1px solid rgba(239, 68, 68, 0.3);
  border-radius: 0.5rem;
  color: rgb(248, 113, 113);
  font-size: 0.875rem;
  display: flex;
  align-items: center;
  backdrop-filter: blur(10px);
}

/* Container Styles */
.contact-form-container,
.contact-info-container {
  background: linear-gradient(
    145deg,
    rgba(15, 23, 42, 0.8),
    rgba(30, 41, 59, 0.8)
  );
  backdrop-filter: blur(15px);
  padding: 3rem;
  margin-top: 1rem;
  border-radius: 2rem;
  border: 1px solid rgba(148, 163, 184, 0.2);
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
  position: relative;
  overflow: hidden;
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
}

.contact-form-container {
  width: 600px;
}

.contact-info-container {
  width: 500px;
}

.contact-form-container::before,
.contact-info-container::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 3px;
  background: linear-gradient(90deg, #3b82f6, #8b5cf6, #10b981);
  border-radius: 2rem 2rem 0 0;
}

.contact-form-container:hover,
.contact-info-container:hover {
  transform: translateY(-5px);
  box-shadow: 0 30px 60px rgba(0, 0, 0, 0.4);
  border-color: rgba(99, 102, 241, 0.3);
}

/* Form Styles */
.form-group {
  margin-bottom: 2rem;
  position: relative;
}

.form-label {
  display: block;
  margin-bottom: 0.75rem;
  font-weight: 600;
  color: rgb(226, 232, 240);
  font-size: 0.95rem;
  text-transform: uppercase;
  letter-spacing: 0.5px;
}

.form-input {
  width: 100%;
  padding: 1rem 1.25rem;
  background: linear-gradient(
    135deg,
    rgba(31, 41, 55, 0.8),
    rgba(55, 65, 81, 0.8)
  );
  backdrop-filter: blur(10px);
  border: 1px solid rgba(75, 85, 99, 0.5);
  border-radius: 1rem;
  color: white;
  font-size: 1rem;
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  position: relative;
}

.form-input:focus {
  outline: none;
  border-color: rgb(99, 102, 241);
  box-shadow: 0 0 0 3px rgba(99, 102, 241, 0.2);
  transform: translateY(-2px);
  background: linear-gradient(
    135deg,
    rgba(31, 41, 55, 0.9),
    rgba(55, 65, 81, 0.9)
  );
}

.form-input.border-red-500 {
  border-color: rgb(239, 68, 68);
  box-shadow: 0 0 0 3px rgba(239, 68, 68, 0.2);
}

.form-input.border-green-500 {
  border-color: rgb(34, 197, 94);
  box-shadow: 0 0 0 3px rgba(34, 197, 94, 0.1);
}

.form-input::placeholder {
  color: rgb(156, 163, 175);
  transition: color 0.3s ease;
}

.form-input:focus::placeholder {
  color: rgb(107, 114, 128);
}

/* Submit Button */
.submit-button {
  width: 100%;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  padding: 1rem 2rem;
  border: none;
  border-radius: 1rem;
  font-weight: 700;
  font-size: 1.1rem;
  cursor: pointer;
  position: relative;
  overflow: hidden;
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  text-transform: uppercase;
  letter-spacing: 0.5px;
  box-shadow: 0 10px 25px rgba(102, 126, 234, 0.3);
}

.submit-button::before {
  content: "";
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(
    90deg,
    transparent,
    rgba(255, 255, 255, 0.2),
    transparent
  );
  transition: left 0.6s ease;
}

.submit-button:hover:not(:disabled) {
  transform: translateY(-3px) scale(1.02);
  box-shadow: 0 20px 40px rgba(102, 126, 234, 0.4);
  background: linear-gradient(135deg, #7c3aed 0%, #8b5cf6 100%);
}

.submit-button:hover:not(:disabled)::before {
  left: 100%;
}

.submit-button:disabled {
  opacity: 0.7;
  cursor: not-allowed;
  transform: none;
}

.button-glow {
  position: absolute;
  inset: 0;
  border-radius: 1rem;
  padding: 2px;
  background: linear-gradient(45deg, #3b82f6, #8b5cf6, #10b981, #f59e0b);
  mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
  mask-composite: exclude;
  opacity: 0;
  transition: opacity 0.3s ease;
}

.submit-button:hover .button-glow {
  opacity: 0.6;
}

/* Contact Items */
.contact-item {
  display: flex;
  align-items: flex-start;
  gap: 1.5rem;
  padding: 1.5rem;
  border-radius: 1rem;
  background: linear-gradient(
    135deg,
    rgba(31, 41, 55, 0.4),
    rgba(55, 65, 81, 0.4)
  );
  backdrop-filter: blur(10px);
  border: 1px solid rgba(75, 85, 99, 0.3);
  transition: all 0.3s ease;
  margin-bottom: 1rem;
  opacity: 0;
  transform: translateY(20px);
}

.contact-item.animate-in {
  opacity: 1;
  transform: translateY(0);
}

.contact-item:hover {
  transform: translateY(-3px);
  border-color: rgba(99, 102, 241, 0.4);
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
}

.contact-icon {
  width: 3.5rem;
  height: 3.5rem;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  border-radius: 1rem;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  flex-shrink: 0;
  font-size: 1.25rem;
  box-shadow: 0 8px 25px rgba(102, 126, 234, 0.3);
  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
}

.contact-icon::before {
  content: "";
  position: absolute;
  inset: 0;
  background: linear-gradient(45deg, rgba(255, 255, 255, 0.3), transparent);
  opacity: 0;
  transition: opacity 0.3s ease;
}

.contact-item:hover .contact-icon {
  transform: scale(1.1) rotate(5deg);
  box-shadow: 0 15px 35px rgba(102, 126, 234, 0.4);
}

.contact-item:hover .contact-icon::before {
  opacity: 1;
}

.contact-item h3 {
  color: white;
  margin-bottom: 0.5rem;
  font-weight: 600;
}

.contact-item a {
  color: rgb(203, 213, 225);
  transition: color 0.3s ease;
}

.contact-item:hover a {
  color: rgb(99, 102, 241);
}

/* Social Links */
.social-links {
  margin-top: 2rem;
  padding-top: 2rem;
  border-top: 1px solid rgba(75, 85, 99, 0.3);
}

.social-link {
  width: 3.5rem;
  height: 3.5rem;
  border-radius: 1rem;
  display: flex;
  align-items: center;
  justify-content: center;
  color: rgb(156, 163, 175);
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  position: relative;
  overflow: hidden;
  font-size: 1.25rem;
  border: 1px solid rgba(75, 85, 99, 0.3);
  background: linear-gradient(
    135deg,
    rgba(31, 41, 55, 0.6),
    rgba(55, 65, 81, 0.6)
  );
  backdrop-filter: blur(10px);
}

.social-link::before {
  content: "";
  position: absolute;
  inset: 0;
  background: linear-gradient(135deg, var(--social-color), transparent);
  opacity: 0;
  transition: opacity 0.3s ease;
}

.social-link:hover {
  color: white;
  transform: translateY(-3px) scale(1.1);
  border-color: var(--social-color);
  box-shadow: 0 10px 25px rgba(var(--social-rgb), 0.4);
}

.social-link:hover::before {
  opacity: 0.2;
}

/* Quick Answers Styles */
.quick-answers-section {
  opacity: 0;
  transform: translateY(20px);
  animation: fadeInUp 0.8s ease-out 1s forwards;
}

.quick-answer-btn {
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  cursor: pointer;
}

.quick-answer-btn:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 25px rgba(59, 130, 246, 0.15);
  background: linear-gradient(
    135deg,
    rgba(59, 130, 246, 0.1),
    rgba(147, 51, 234, 0.1)
  );
}

.quick-answer-btn:active {
  transform: translateY(0);
  transition-duration: 0.1s;
}

/* Social Media Color Variables */
.social-link.github {
  --social-color: #333;
  --social-rgb: 51, 51, 51;
}

.social-link.linkedin {
  --social-color: #0077b5;
  --social-rgb: 0, 119, 181;
}

.social-link.twitter {
  --social-color: #1da1f2;
  --social-rgb: 29, 161, 242;
}

.social-link.instagram {
  --social-color: #e4405f;
  --social-rgb: 228, 64, 95;
}

.social-link.facebook {
  --social-color: #1877f2;
  --social-rgb: 24, 119, 242;
}

.social-link.discord {
  --social-color: #5865f2;
  --social-rgb: 88, 101, 242;
}

.social-link.youtube {
  --social-color: #ff0000;
  --social-rgb: 255, 0, 0;
}

.social-link.telegram {
  --social-color: #0088cc;
  --social-rgb: 0, 136, 204;
}

.social-link.whatsapp {
  --social-color: #25d366;
  --social-rgb: 37, 211, 102;
}

.tooltip {
  position: absolute;
  bottom: 120%;
  left: 50%;
  transform: translateX(-50%);
  background: rgba(17, 24, 39, 0.9);
  color: white;
  padding: 0.5rem 0.75rem;
  border-radius: 0.5rem;
  font-size: 0.75rem;
  font-weight: 500;
  opacity: 0;
  pointer-events: none;
  transition: opacity 0.3s ease;
  backdrop-filter: blur(10px);
  border: 1px solid rgba(75, 85, 99, 0.3);
}

.social-link:hover .tooltip {
  opacity: 1;
}

/* Status and FAQ */
.availability-status {
  margin-top: 2rem;
  padding-top: 2rem;
  border-top: 1px solid rgba(75, 85, 99, 0.3);
}

.status-indicator {
  display: flex;
  align-items: center;
  gap: 1rem;
  padding: 1rem;
  background: linear-gradient(
    135deg,
    rgba(34, 197, 94, 0.1),
    rgba(16, 185, 129, 0.1)
  );
  border-radius: 1rem;
  border: 1px solid rgba(34, 197, 94, 0.2);
}

.status-dot {
  width: 1rem;
  height: 1rem;
  background: linear-gradient(135deg, #22c55e, #10b981);
  border-radius: 50%;
  animation: pulse 2s infinite;
  box-shadow: 0 0 15px rgba(34, 197, 94, 0.5);
}

.status-text {
  font-weight: 600;
  color: rgb(34, 197, 94);
}

@keyframes pulse {
  0%,
  100% {
    opacity: 1;
    transform: scale(1);
  }
  50% {
    opacity: 0.7;
    transform: scale(1.1);
  }
}

.faq-section {
  margin-top: 2rem;
  padding-top: 2rem;
  border-top: 1px solid rgba(75, 85, 99, 0.3);
}

.faq-item {
  margin-top: 10px;
  background: linear-gradient(
    135deg,
    rgba(31, 41, 55, 0.6),
    rgba(55, 65, 81, 0.6)
  );
  backdrop-filter: blur(10px);
  padding: 1.5rem;
  border-radius: 1rem;
  margin-bottom: 1rem;
  border: 1px solid rgba(75, 85, 99, 0.3);
  transition: all 0.3s ease;
  opacity: 0;
  transform: translateY(20px);
}

.faq-item.animate-in {
  opacity: 1;
  transform: translateY(0);
}

.faq-item:hover {
  transform: translateY(-2px);
  border-color: rgba(99, 102, 241, 0.4);
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2);
}

.faq-item h4 {
  color: white;
  margin-bottom: 0.75rem;
}

.faq-item p {
  color: rgb(203, 213, 225);
  line-height: 1.5;
}

/* Keyboard shortcut styling */
.kbd {
  background: linear-gradient(
    135deg,
    rgba(31, 41, 55, 0.8),
    rgba(55, 65, 81, 0.8)
  );
  border: 1px solid rgba(75, 85, 99, 0.5);
  border-radius: 0.25rem;
  padding: 0.125rem 0.375rem;
  font-family: monospace;
  font-size: 0.75rem;
  color: rgb(203, 213, 225);
}

/* Responsive Design */
@media (max-width: 768px) {
  .contact-form-container,
  .contact-info-container {
    padding: 2rem 1.5rem;
    width: 100%;
  }

  .header-section h1 {
    font-size: 2.5rem;
  }

  .header-section p {
    font-size: 1rem;
  }

  .contact-item {
    flex-direction: column;
    text-align: center;
    gap: 1rem;
    padding: 1rem;
  }

  .contact-icon {
    margin: 0 auto;
  }

  .faq-item h4 {
    flex-direction: column;
    gap: 0.5rem;
    align-items: flex-start;
  }

  .faq-item p {
    margin-left: 0;
  }

  .form-input {
    padding: 0.875rem 1rem;
  }

  .submit-button {
    padding: 0.875rem 1.5rem;
    font-size: 1rem;
  }

  .quick-answer-btn {
    padding: 0.75rem;
  }

  .quick-answer-btn h4 {
    font-size: 0.875rem;
  }

  .quick-answer-btn p {
    font-size: 0.75rem;
  }

  .social-links .grid {
    grid-template-columns: repeat(3, 1fr);
    gap: 0.75rem;
  }

  .social-link {
    width: 3rem;
    height: 3rem;
    font-size: 1rem;
  }

  /* Toast notifications for mobile */
  .fixed.top-6.right-6 {
    top: 1rem;
    right: 1rem;
    left: 1rem;
    right: 1rem;
  }
}

@media (max-width: 480px) {
  .header-section h1 {
    font-size: 2rem;
  }

  .contact-form-container,
  .contact-info-container {
    padding: 1.5rem 1rem;
  }
}

/* Reduced motion accessibility */
@media (prefers-reduced-motion: reduce) {
  * {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
  }
}
</style>
