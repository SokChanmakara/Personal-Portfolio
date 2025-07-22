<template>
  <div class="min-h-screen text-white">
    <div class="container mx-auto px-6 py-16">
      <!-- Header Section -->
      <div class="text-center mb-16">
        <h1 class="text-5xl font-bold mb-4">Resume</h1>
        <p class="text-xl text-gray-400 max-w-3xl mx-auto mb-8">
          A comprehensive overview of my professional experience, education, and
          skills
        </p>
        <button
          class="bg-gradient-to-r from-blue-500 to-purple-600 text-white px-6 py-3 rounded-lg font-semibold hover:from-blue-600 hover:to-purple-700 transition-all duration-300"
        >
          <i class="fas fa-download mr-2"></i>
          Download PDF
        </button>
      </div>

      <div class="grid grid-cols-1 lg:grid-cols-3 gap-12">
        <!-- Left Column -->
        <div class="lg:col-span-2 space-y-12">
          <!-- Professional Experience -->
          <section>
            <h2 class="text-3xl font-bold mb-8 text-blue-400">
              Professional Experience
            </h2>

            <!-- Job 1 -->
            <div class="experience-item">
              <div class="experience-header">
                <h3 class="text-xl font-bold">Senior Full Stack Developer</h3>
                <div class="company-info">
                  <span class="company-name">TechCorp Solutions</span>
                  <span class="duration">2023 - Present</span>
                </div>
              </div>
              <ul class="experience-details">
                <li>
                  Led development of enterprise-level web applications serving
                  10,000+ users
                </li>
                <li>
                  Implemented microservices architecture improving system
                  performance by 40%
                </li>
                <li>Mentored junior developers and conducted code reviews</li>
                <li>
                  Collaborated with cross-functional teams to deliver projects
                  on time
                </li>
              </ul>
            </div>

            <!-- Job 2 -->
            <div class="experience-item">
              <div class="experience-header">
                <h3 class="text-xl font-bold">Full Stack Developer</h3>
                <div class="company-info">
                  <span class="company-name">Digital Innovations Ltd</span>
                  <span class="duration">2022 - 2023</span>
                </div>
              </div>
              <ul class="experience-details">
                <li>
                  Developed responsive web applications using Vue.js and Node.js
                </li>
                <li>Integrated third-party APIs and payment gateways</li>
                <li>Optimized database queries reducing load times by 60%</li>
                <li>
                  Participated in agile development processes and daily standups
                </li>
              </ul>
            </div>

            <!-- Job 3 -->
            <div class="experience-item">
              <div class="experience-header">
                <h3 class="text-xl font-bold">Frontend Developer</h3>
                <div class="company-info">
                  <span class="company-name">StartupHub</span>
                  <span class="duration">2021 - 2022</span>
                </div>
              </div>
              <ul class="experience-details">
                <li>
                  Built modern, responsive user interfaces using React and
                  Vue.js
                </li>
                <li>
                  Collaborated with designers to implement pixel-perfect designs
                </li>
                <li>Improved website performance and accessibility scores</li>
                <li>Maintained and updated existing codebases</li>
              </ul>
            </div>
          </section>

          <!-- Education -->
          <section>
            <h2 class="text-3xl font-bold mb-8 text-green-400">Education</h2>

            <div class="education-item">
              <div class="education-header">
                <h3 class="text-xl font-bold">
                  Bachelor of Science in Computer Science
                </h3>
                <div class="education-info">
                  <span class="university">University of Technology</span>
                  <span class="duration">2017 - 2021</span>
                </div>
              </div>
              <p class="education-details">
                Graduated with honors. Relevant coursework: Data Structures,
                Algorithms, Web Development, Database Systems, Software
                Engineering.
              </p>
            </div>
          </section>

          <!-- Certifications -->
          <section>
            <h2 class="text-3xl font-bold mb-8 text-purple-400">
              Certifications
            </h2>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
              <div class="certification-item">
                <h3 class="font-bold">AWS Certified Developer</h3>
                <p class="text-gray-400">Amazon Web Services • 2023</p>
              </div>
              <div class="certification-item">
                <h3 class="font-bold">Vue.js 3 Certification</h3>
                <p class="text-gray-400">Vue School • 2023</p>
              </div>
              <div class="certification-item">
                <h3 class="font-bold">Google Analytics Certified</h3>
                <p class="text-gray-400">Google • 2022</p>
              </div>
              <div class="certification-item">
                <h3 class="font-bold">Scrum Master Certified</h3>
                <p class="text-gray-400">Scrum Alliance • 2022</p>
              </div>
            </div>
          </section>
        </div>

        <!-- Right Column -->
        <div class="space-y-12">
          <!-- Skills -->
          <section>
            <h2 class="text-2xl font-bold mb-6">Technical Skills</h2>

            <div class="skill-category">
              <h3 class="text-lg font-semibold mb-4 text-blue-400">Frontend</h3>
              <div class="skill-list">
                <div class="skill-item">
                  <span>Vue.js</span>
                  <div class="skill-bar">
                    <div class="skill-progress" style="width: 95%"></div>
                  </div>
                </div>
                <div class="skill-item">
                  <span>React</span>
                  <div class="skill-bar">
                    <div class="skill-progress" style="width: 90%"></div>
                  </div>
                </div>
                <div class="skill-item">
                  <span>TypeScript</span>
                  <div class="skill-bar">
                    <div class="skill-progress" style="width: 85%"></div>
                  </div>
                </div>
                <div class="skill-item">
                  <span>Tailwind CSS</span>
                  <div class="skill-bar">
                    <div class="skill-progress" style="width: 92%"></div>
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
                    <div class="skill-progress" style="width: 88%"></div>
                  </div>
                </div>
                <div class="skill-item">
                  <span>Python</span>
                  <div class="skill-bar">
                    <div class="skill-progress" style="width: 82%"></div>
                  </div>
                </div>
                <div class="skill-item">
                  <span>Express.js</span>
                  <div class="skill-bar">
                    <div class="skill-progress" style="width: 85%"></div>
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
                  <span>MongoDB</span>
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
          <section>
            <h2 class="text-2xl font-bold mb-6">Languages</h2>
            <div class="space-y-4">
              <div class="language-item">
                <div class="flex justify-between mb-2">
                  <span>English</span>
                  <span class="text-gray-400">Fluent</span>
                </div>
                <div class="skill-bar">
                  <div class="skill-progress" style="width: 95%"></div>
                </div>
              </div>
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
                  <span>French</span>
                  <span class="text-gray-400">Basic</span>
                </div>
                <div class="skill-bar">
                  <div class="skill-progress" style="width: 40%"></div>
                </div>
              </div>
            </div>
          </section>

          <!-- Interests -->
          <section>
            <h2 class="text-2xl font-bold mb-6">Interests</h2>
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
import { onMounted } from "vue";

onMounted(() => {
  // Add any animations or interactions here
});
</script>

<style scoped>
.experience-item,
.education-item {
  background-color: black;
  padding: 2rem;
  border-radius: 1rem;
  border: 1px solid rgb(31, 41, 55);
  margin-bottom: 2rem;
}

.experience-header,
.education-header {
  margin-bottom: 1rem;
}

.company-info,
.education-info {
  display: flex;
  justify-content: between;
  flex-wrap: wrap;
  gap: 1rem;
  margin-top: 0.5rem;
}

.company-name,
.university {
  color: rgb(156, 163, 175);
  font-weight: 500;
}

.duration {
  color: rgb(34, 197, 94);
  font-weight: 500;
  margin-left: auto;
}

.experience-details {
  list-style: none;
  padding: 0;
  margin: 0;
}

.experience-details li {
  padding: 0.5rem 0;
  padding-left: 1.5rem;
  position: relative;
  color: rgb(209, 213, 219);
}

.experience-details li::before {
  content: "•";
  color: rgb(99, 102, 241);
  position: absolute;
  left: 0;
  font-weight: bold;
}

.education-details {
  color: rgb(209, 213, 219);
  line-height: 1.6;
}

.certification-item {
  background-color: rgb(17, 24, 39);
  padding: 1.5rem;
  border-radius: 0.75rem;
  border: 1px solid rgb(31, 41, 55);
}

.skill-category {
  margin-bottom: 2rem;
}

.skill-list {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.skill-item {
  margin-bottom: 1rem;
}

.skill-item span {
  display: block;
  margin-bottom: 0.5rem;
  font-weight: 500;
}

.skill-bar {
  width: 100%;
  height: 0.5rem;
  background-color: rgb(31, 41, 55);
  border-radius: 0.25rem;
  overflow: hidden;
}

.skill-progress {
  height: 100%;
  background: linear-gradient(90deg, #3b82f6, #8b5cf6);
  border-radius: 0.25rem;
  transition: width 0.3s ease;
}

.language-item {
  margin-bottom: 1rem;
}

.interest-tag {
  background-color: rgb(17, 24, 39);
  color: rgb(209, 213, 219);
  padding: 0.5rem 1rem;
  border-radius: 1.5rem;
  border: 1px solid rgb(31, 41, 55);
  font-size: 0.875rem;
  display: inline-flex;
  align-items: center;
}

@media (max-width: 768px) {
  .company-info,
  .education-info {
    flex-direction: column;
    gap: 0.5rem;
  }

  .duration {
    margin-left: 0;
  }
}
</style>
