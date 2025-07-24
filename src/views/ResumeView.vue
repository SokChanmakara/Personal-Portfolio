<template>
  <div class="min-h-screen text-white">
    <div class="container mx-auto px-6 py-16">
      <!-- Header Section -->
      <div class="text-center mb-16">
        <div class="relative">
          <h1
            class="text-6xl font-bold mb-6 bg-gradient-to-r from-blue-400 via-purple-500 to-emerald-400 bg-clip-text text-transparent"
          >
            Resume
          </h1>
        </div>
      </div>

      <div class="grid grid-cols-1 lg:grid-cols-3 gap-12">
        <!-- Left Column -->
        <div class="lg:col-span-2 space-y-12">
          <!-- Professional Experience -->
          <section class="group">
            <div class="flex items-center mb-8">
              <h2 class="text-3xl font-bold text-blue-400">Experience</h2>
            </div>

            <!-- Job 1 -->
            <div class="experience-item">
              <div class="experience-header">
                <h3 class="text-xl font-bold">Freelance Developer</h3>
                <div class="company-info">
                  <span class="company-name">Codera Club</span>
                  <span class="duration">May 2025 - Present</span>
                </div>
              </div>
              <ul class="experience-details">
                <li>Mobile Developer for Codera Club</li>
                <li>Have Experience build an Education App</li>
                <li>
                  Applied state management using Provider/Riverpod to ensure
                  responsive and maintainable UI logic.
                </li>
                <li>
                  Collaborated with backend developers to consume REST APIs for
                  dynamic content.
                </li>
              </ul>
            </div>

            <!-- Job 2 -->
            <div class="experience-item">
              <div class="experience-header">
                <h3 class="text-xl font-bold">IT Support Internship</h3>
                <div class="company-info">
                  <span class="company-name">SNKRP</span>
                  <span class="duration">Aug 2024 - Oct 2024</span>
                </div>
              </div>
              <ul class="experience-details">
                <li>
                  Helped setup and maintain employee records on the server.
                </li>
                <li>
                  Hands-On Experienced in using Synology server for storage and
                  file management.
                </li>
                <li>
                  Configured network infrastructure including Wi-Fi, routers,
                  subnets, and DNS; implemented social media access restrictions
                  for the company.
                </li>
              </ul>
            </div>

            <!-- Job 3 -->
            <div class="experience-item">
              <div class="experience-header">
                <h3 class="text-xl font-bold">Content Writer</h3>
                <div class="company-info">
                  <span class="company-name">Westec Media</span>
                  <span class="duration">Jan 2023 - Oct 2024</span>
                </div>
              </div>
              <ul class="experience-details">
                <li>Collect and Analyse movies source</li>
                <li>
                  Make Recommendations on improvement based on my analysis and
                  write a content
                </li>
                <li>Communication and Teamwork</li>
              </ul>
            </div>
          </section>

          <!-- Education -->
          <section class="group">
            <div class="flex items-center mb-8">
              <h2 class="text-3xl font-bold text-green-400">Education</h2>
            </div>

            <div class="education-item">
              <div class="education-header">
                <h3 class="text-xl font-bold">
                  Information and Communication Engineering
                </h3>
                <div class="education-info">
                  <span class="university"
                    >Institute of Technology of Cambodia</span
                  >
                  <span class="duration">2021 - Present</span>
                </div>
              </div>
              <p class="education-details">
                Relevant coursework: Data Structures, Algorithms, Web
                Development, MObile Devlopement, Database Systems, Software
                Engineering.
              </p>
            </div>
          </section>
          <!-- Diploma -->
          <section class="group">
            <div class="education-item">
              <div class="education-header">
                <h3 class="text-xl font-bold">High School</h3>
                <div class="education-info">
                  <span class="university">Sonthormok High School</span>
                  <span class="duration">2018 - 2021</span>
                </div>
              </div>
              <p class="education-details">General knowledge</p>
            </div>
          </section>
        </div>

        <!-- Right Column -->
        <div class="space-y-12">
          <!-- Skills -->
          <section class="sticky top-8">
            <div class="flex items-center mb-6">
              <h2 class="text-2xl font-bold">Technical Skills</h2>
            </div>

            <div class="skill-category">
              <h3 class="text-lg font-semibold mb-4 text-blue-400">Frontend</h3>
              <div class="skill-list">
                <div class="skill-item">
                  <span>Vue.js</span>
                  <div class="skill-bar">
                    <div class="skill-progress" style="width: 70%"></div>
                  </div>
                </div>
                <div class="skill-item">
                  <span>HTML</span>
                  <div class="skill-bar">
                    <div class="skill-progress" style="width: 85%"></div>
                  </div>
                </div>
                <div class="skill-item">
                  <span>CSS</span>
                  <div class="skill-bar">
                    <div class="skill-progress" style="width: 75%"></div>
                  </div>
                </div>
                <div class="skill-item">
                  <span>JavaScript</span>
                  <div class="skill-bar">
                    <div class="skill-progress" style="width: 70%"></div>
                  </div>
                </div>
                <div class="skill-item">
                  <span>Tailwind CSS</span>
                  <div class="skill-bar">
                    <div class="skill-progress" style="width: 65%"></div>
                  </div>
                </div>
              </div>
            </div>

            <div class="skill-category">
              <h3 class="text-lg font-semibold mb-4 text-green-400">Backend</h3>
              <div class="skill-list">
                <div class="skill-item">
                  <span>Node.js</span>
                  <div class="skill-bar">
                    <div class="skill-progress" style="width: 60%"></div>
                  </div>
                </div>
                <div class="skill-item">
                  <span>Laravel</span>
                  <div class="skill-bar">
                    <div class="skill-progress" style="width: 82%"></div>
                  </div>
                </div>
                <div class="skill-item">
                  <span>Express.js</span>
                  <div class="skill-bar">
                    <div class="skill-progress" style="width: 70%"></div>
                  </div>
                </div>
                <div class="skill-item">
                  <span>REST APIs</span>
                  <div class="skill-bar">
                    <div class="skill-progress" style="width: 90%"></div>
                  </div>
                </div>
              </div>
            </div>

            <div class="skill-category">
              <h3 class="text-lg font-semibold mb-4 text-purple-400">
                Database & Tools
              </h3>
              <div class="skill-list">
                <div class="skill-item">
                  <span>MySQL</span>
                  <div class="skill-bar">
                    <div class="skill-progress" style="width: 80%"></div>
                  </div>
                </div>
                <div class="skill-item">
                  <span>PostgreSQL</span>
                  <div class="skill-bar">
                    <div class="skill-progress" style="width: 75%"></div>
                  </div>
                </div>
                <div class="skill-item">
                  <span>Git/GitHub</span>
                  <div class="skill-bar">
                    <div class="skill-progress" style="width: 93%"></div>
                  </div>
                </div>
                <div class="skill-item">
                  <span>Docker</span>
                  <div class="skill-bar">
                    <div class="skill-progress" style="width: 78%"></div>
                  </div>
                </div>
              </div>
            </div>
          </section>

          <!-- Languages -->
          <section class="language-section">
            <div class="flex items-center mb-6">
              <h2 class="text-2xl font-bold">Languages</h2>
            </div>
            <div class="space-y-4">
              <div class="language-item">
                <div class="flex justify-between mb-2">
                  <span>Khmer</span>
                  <span class="text-gray-400">Native</span>
                </div>
                <div class="skill-bar">
                  <div class="skill-progress" style="width: 100%"></div>
                </div>
              </div>
              <div class="language-item">
                <div class="flex justify-between mb-2">
                  <span>English</span>
                  <span class="text-gray-400">Fluent</span>
                </div>
                <div class="skill-bar">
                  <div class="skill-progress" style="width: 90%"></div>
                </div>
              </div>
              <div class="language-item">
                <div class="flex justify-between mb-2">
                  <span>French</span>
                  <span class="text-gray-400">Basic</span>
                </div>
                <div class="skill-bar">
                  <div class="skill-progress" style="width: 20%"></div>
                </div>
              </div>
            </div>
          </section>

          <!-- Interests -->
          <section>
            <div class="flex items-center mb-6" style="margin-bottom: 24px">
              <h2 class="text-2xl font-bold">Interests</h2>
            </div>
            <div class="flex flex-wrap gap-3">
              <span class="interest-tag">
                <i class="fas fa-code mr-2"></i>
                Coding
              </span>
              <span class="interest-tag">
                <i class="fas fa-camera mr-2"></i>
                Photography
              </span>
              <span class="interest-tag">
                <i class="fas fa-music mr-2"></i>
                Music
              </span>
              <span class="interest-tag">
                <i class="fas fa-gamepad mr-2"></i>
                Gaming
              </span>
              <span class="interest-tag">
                <i class="fas fa-plane mr-2"></i>
                Travel
              </span>
              <span class="interest-tag">
                <i class="fas fa-book mr-2"></i>
                Reading
              </span>
            </div>
          </section>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { onMounted, ref } from "vue";

const skillsVisible = ref(false);

onMounted(() => {
  // Add intersection observer for skill bars animation
  const observer = new IntersectionObserver(
    (entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.style.opacity = "1";
          entry.target.style.transform = "translateY(0)";

          // Animate skill bars when they come into view
          if (
            entry.target.classList.contains("skill-category") ||
            entry.target.classList.contains("language-section")
          ) {
            skillsVisible.value = true;
            const skillBars = entry.target.querySelectorAll(".skill-progress");
            skillBars.forEach((bar, index) => {
              setTimeout(() => {
                bar.style.animation = "fillBar 1.5s ease-out forwards";
              }, index * 100);
            });
          }
        }
      });
    },
    {
      threshold: 0.1,
      rootMargin: "0px 0px -100px 0px",
    }
  );

  // Observe all sections
  const sections = document.querySelectorAll(
    ".experience-item, .education-item, .certification-item, .skill-category, .language-section"
  );
  sections.forEach((section) => {
    observer.observe(section);
  });

  // Add CSS for skill bar animation
  const style = document.createElement("style");
  style.textContent = `
    @keyframes fillBar {
      from {
        width: 0;
      }
      to {
        width: var(--target-width);
      }
    }
  `;
  document.head.appendChild(style);

  // Set CSS custom properties for skill bar widths
  setTimeout(() => {
    const skillBars = document.querySelectorAll(".skill-progress");
    skillBars.forEach((bar) => {
      const width = bar.style.width;
      bar.style.setProperty("--target-width", width);
      bar.style.width = "0";
    });
  }, 100);
});
</script>

<style scoped>
.experience-item,
.education-item {
  margin-top: 16px;
  background: linear-gradient(
    135deg,
    rgba(15, 23, 42, 0.8),
    rgba(30, 41, 59, 0.8)
  );
  backdrop-filter: blur(10px);
  padding: 2.5rem;
  border-radius: 1.5rem;
  border: 1px solid rgba(148, 163, 184, 0.1);
  margin-bottom: 2rem;
  position: relative;
  overflow: hidden;
  transition: all 0.3s ease;
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
}

.experience-item:hover,
.education-item:hover {
  transform: translateY(-5px);
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
  border-color: rgba(99, 102, 241, 0.3);
}

.experience-item::before,
.education-item::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 3px;
  background: linear-gradient(90deg, #3b82f6, #8b5cf6, #10b981);
  border-radius: 1.5rem 1.5rem 0 0;
}

.experience-header,
.education-header {
  margin-bottom: 1.5rem;
}

.company-info,
.education-info {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 1rem;
  margin-top: 0.75rem;
  align-items: center;
}

.company-name,
.university {
  color: rgb(148, 163, 184);
  font-weight: 600;
  font-size: 1.1rem;
}

.duration {
  background: linear-gradient(135deg, #10b981, #059669);
  color: white;
  font-weight: 600;
  padding: 0.5rem 1rem;
  border-radius: 1rem;
  font-size: 0.9rem;
  box-shadow: 0 4px 12px rgba(16, 185, 129, 0.3);
}

.experience-details {
  list-style: none;
  padding: 0;
  margin: 0;
  margin-top: 1.5rem;
}

.experience-details li {
  padding: 0.75rem 0;
  padding-left: 2rem;
  position: relative;
  color: rgb(203, 213, 225);
  line-height: 1.6;
  transition: color 0.2s ease;
}

.experience-details li:hover {
  color: rgb(226, 232, 240);
}

.experience-details li::before {
  content: "→";
  color: #3b82f6;
  position: absolute;
  left: 0;
  font-weight: bold;
  font-size: 1.2rem;
  transition: transform 0.2s ease;
}

.experience-details li:hover::before {
  transform: translateX(3px);
}

.education-details {
  color: rgb(203, 213, 225);
  line-height: 1.7;
  margin-top: 1rem;
  font-size: 1.05rem;
}

.certification-item {
  background: linear-gradient(
    135deg,
    rgba(17, 24, 39, 0.9),
    rgba(31, 41, 55, 0.9)
  );
  backdrop-filter: blur(10px);
  padding: 2rem;
  border-radius: 1rem;
  border: 1px solid rgba(148, 163, 184, 0.1);
  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
}

.certification-item:hover {
  transform: translateY(-3px);
  box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
  border-color: rgba(139, 92, 246, 0.3);
}

.certification-item::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 2px;
  background: linear-gradient(90deg, #8b5cf6, #a855f7);
}

.certification-item h3 {
  color: #e2e8f0;
  margin-bottom: 0.5rem;
}

.skill-category {
  margin-bottom: 3rem;
  padding: 2rem;
  margin-top: 1rem;
  background: linear-gradient(
    135deg,
    rgba(15, 23, 42, 0.6),
    rgba(30, 41, 59, 0.6)
  );
  backdrop-filter: blur(10px);
  border-radius: 1.5rem;
  border: 1px solid rgba(148, 163, 184, 0.1);
  transition: all 0.3s ease;
}

.skill-category:hover {
  transform: translateY(-2px);
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.15);
}

.skill-list {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.skill-item {
  position: relative;
}

.skill-item span {
  display: block;
  margin-bottom: 0.75rem;
  font-weight: 600;
  color: #e2e8f0;
  font-size: 1.05rem;
}

.skill-bar {
  width: 100%;
  height: 0.75rem;
  background-color: rgba(51, 65, 85, 0.8);
  border-radius: 0.5rem;
  overflow: hidden;
  position: relative;
  box-shadow: inset 0 2px 4px rgba(0, 0, 0, 0.2);
}

.skill-progress {
  height: 100%;
  background: linear-gradient(90deg, #3b82f6, #8b5cf6, #10b981);
  border-radius: 0.5rem;
  transition: all 0.8s cubic-bezier(0.4, 0, 0.2, 1);
  position: relative;
  overflow: hidden;
}

.skill-progress::after {
  content: "";
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(
    90deg,
    transparent,
    rgba(255, 255, 255, 0.3),
    transparent
  );
  animation: shimmer 2s infinite;
}

@keyframes shimmer {
  0% {
    left: -100%;
  }
  100% {
    left: 100%;
  }
}

.language-item {
  margin-bottom: 1.5rem;
  padding: 1rem;
  background: linear-gradient(
    135deg,
    rgba(15, 23, 42, 0.4),
    rgba(30, 41, 59, 0.4)
  );
  border-radius: 1rem;
  border: 1px solid rgba(148, 163, 184, 0.1);
  transition: all 0.3s ease;
}

.language-item:hover {
  transform: translateX(5px);
  border-color: rgba(59, 130, 246, 0.3);
}

.interest-tag {
  background: linear-gradient(
    135deg,
    rgba(17, 24, 39, 0.9),
    rgba(31, 41, 55, 0.9)
  );
  backdrop-filter: blur(10px);
  color: rgb(226, 232, 240);
  padding: 0.75rem 1.5rem;
  border-radius: 2rem;
  border: 1px solid rgba(148, 163, 184, 0.2);
  font-size: 0.95rem;
  font-weight: 500;
  display: inline-flex;
  align-items: center;
  transition: all 0.3s ease;
  cursor: pointer;
}

.interest-tag:hover {
  transform: translateY(-2px) scale(1.05);
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2);
  border-color: rgba(236, 72, 153, 0.4);
  background: linear-gradient(
    135deg,
    rgba(236, 72, 153, 0.2),
    rgba(219, 39, 119, 0.2)
  );
}

.interest-tag i {
  margin-right: 0.5rem;
  color: #f472b6;
}

/* Section animations */
.group {
  opacity: 0;
  animation: fadeInUp 0.8s ease forwards;
}

.group:nth-child(1) {
  animation-delay: 0.1s;
}
.group:nth-child(2) {
  animation-delay: 0.2s;
}
.group:nth-child(3) {
  animation-delay: 0.3s;
}

@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* Responsive improvements */
@media (max-width: 1024px) {
  .container {
    padding: 1.5rem;
  }

  .text-center h1 {
    font-size: 4rem;
  }

  .experience-item,
  .education-item {
    padding: 2rem;
  }

  .skill-category {
    padding: 1.75rem;
  }
}

@media (max-width: 768px) {
  .container {
    padding: 1rem;
  }

  .text-center h1 {
    font-size: 2.5rem;
  }

  .company-info,
  .education-info {
    flex-direction: column;
    gap: 0.75rem;
    align-items: flex-start;
  }

  .duration {
    margin-left: 0;
    align-self: flex-start;
  }

  .experience-item,
  .education-item {
    padding: 2rem;
  }

  .skill-category {
    padding: 1.5rem;
  }

  .experience-header h3,
  .education-header h3 {
    font-size: 1.25rem;
  }

  .company-name,
  .university {
    font-size: 1rem;
  }

  .experience-details li {
    font-size: 0.95rem;
    padding: 0.6rem 0;
  }

  .skill-item span {
    font-size: 1rem;
  }

  .interest-tag {
    padding: 0.6rem 1.25rem;
    font-size: 0.9rem;
  }
}

@media (max-width: 480px) {
  .container {
    padding: 0.75rem;
  }

  .text-center {
    margin-bottom: 2rem;
  }

  .text-center h1 {
    font-size: 2rem;
    margin-bottom: 1rem;
  }

  .experience-item,
  .education-item {
    padding: 1.5rem;
    margin-bottom: 1.5rem;
  }

  .skill-category {
    padding: 1.25rem;
    margin-bottom: 1.5rem;
  }

  .experience-header h3,
  .education-header h3 {
    font-size: 1.1rem;
  }

  .experience-details li {
    font-size: 0.9rem;
    padding: 0.5rem 0;
    padding-left: 1.5rem;
  }

  .skill-item {
    margin-bottom: 1rem;
  }

  .skill-item span {
    font-size: 0.95rem;
    margin-bottom: 0.5rem;
  }

  .skill-bar {
    height: 0.6rem;
  }

  .interest-tag {
    padding: 0.5rem 1rem;
    font-size: 0.85rem;
  }

  .language-item {
    padding: 0.75rem;
    font-size: 0.9rem;
  }

  .section h2 {
    font-size: 1.5rem;
    margin-bottom: 1rem;
  }
}

/* Scroll animations */
@media (prefers-reduced-motion: no-preference) {
  .experience-item,
  .education-item,
  .certification-item {
    opacity: 0;
    animation: slideInFromLeft 0.8s ease forwards;
  }

  .experience-item:nth-child(1) {
    animation-delay: 0.1s;
  }
  .experience-item:nth-child(2) {
    animation-delay: 0.2s;
  }
  .experience-item:nth-child(3) {
    animation-delay: 0.3s;
  }
}

@keyframes slideInFromLeft {
  from {
    opacity: 0;
    transform: translateX(-50px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}
</style>
