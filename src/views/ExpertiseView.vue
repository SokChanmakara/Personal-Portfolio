<template>
  <div class="expertise-container">
    <!-- Header Section -->
    <div class="text-center mb-20" :class="{ 'animate-fade-in': isVisible }">
      <h1 class="main-title">Tech Expertise</h1>
      <p class="subtitle">
        Comprehensive skills across mobile and web development technologies
      </p>
    </div>

    <!-- Mobile Application Development Section -->
    <div class="mb-12">
      <!-- Timeline Container -->
      <div class="timeline">
        <!-- Frameworks / Languages -->
        <div class="timeline-container frameworks">
          <div class="timeline-icon">
            <i class="fas fa-laptop-code"></i>
          </div>
          <div class="timeline-body">
            <h4 class="timeline-title">
              <span class="badge">Frameworks / Languages</span>
            </h4>
            <div class="skill-tags">
              <span class="skill-tag html">
                <img
                  src="../assets/ImageIcon/html.svg"
                  alt=""
                  class="w-8 h-8"
                />
                HTML
              </span>
              <span class="skill-tag css">
                <img src="../assets/ImageIcon/css.svg" alt="" class="w-8 h-8" />
                CSS
              </span>
              <span class="skill-tag javascript">
                <img
                  src="../assets/ImageIcon/javascript.svg"
                  alt=""
                  class="w-8 h-8"
                />
                JavaScript
              </span>
              <span class="skill-tag python">
                <img
                  src="../assets/ImageIcon/python.svg"
                  alt=""
                  class="w-8 h-8"
                />
                Python
              </span>
              <span class="skill-tag vuejs">
                <img src="../assets/ImageIcon/vue.svg" alt="" class="w-8 h-8" />
                VueJS
              </span>
              <span class="skill-tag laravel">
                <img
                  src="../assets/ImageIcon/laravel.svg"
                  alt=""
                  class="w-8 h-8"
                />
                Laravel
              </span>
              <span class="skill-tag flutter">
                <img
                  src="../assets/ImageIcon/flutter.svg"
                  alt=""
                  class="w-8 h-8"
                />
                Flutter
              </span>
              <span class="skill-tag nestjs">
                <img
                  src="../assets/ImageIcon/nestjs.svg"
                  alt=""
                  class="w-8 h-8"
                />
                NestJs
              </span>
              <span class="skill-tag tailwindcss">
                <img
                  src="../assets/ImageIcon/tailwindcss.svg"
                  alt=""
                  class="w-8 h-8"
                />
                TailwindCSS
              </span>
              <span class="skill-tag java">
                <img
                  src="../assets/ImageIcon/java.svg"
                  alt=""
                  class="w-8 h-8"
                />
                Java
              </span>
            </div>
          </div>
        </div>

        <!-- State Management -->
        <div class="timeline-container state-management">
          <div class="timeline-icon">
            <i class="fas fa-layer-group"></i>
          </div>
          <div class="timeline-body">
            <h4 class="timeline-title">
              <span class="badge">State Management</span>
            </h4>
            <div class="skill-tags">
              <span class="skill-tag riverpod">
                <img
                  src="../assets/ImageIcon/riverpod.svg"
                  alt=""
                  class="w-8 h-8"
                />
                Riverpod
              </span>
              <span class="skill-tag pinia">
                <img
                  src="../assets/ImageIcon/pinia.svg"
                  alt=""
                  class="w-8 h-8"
                />
                Pinia
              </span>
            </div>
          </div>
        </div>

        <!-- API Service -->
        <div class="timeline-container api-service">
          <div class="timeline-icon">
            <i class="fas fa-server"></i>
          </div>
          <div class="timeline-body">
            <h4 class="timeline-title">
              <span class="badge">API Service</span>
            </h4>
            <div class="skill-tags">
              <span class="skill-tag rest">
                <img src="../assets/ImageIcon/api.svg" alt="" class="w-8 h-8" />
                REST API
              </span>
              <span class="skill-tag graphql">
                <img
                  src="../assets/ImageIcon/graphql.svg"
                  alt=""
                  class="w-8 h-8"
                />
                GraphQL
              </span>
              <span class="skill-tag postman">
                <img
                  src="../assets/ImageIcon/postman.svg"
                  alt=""
                  class="w-8 h-8"
                />
                Postman
              </span>
              <span class="skill-tag apidog">
                <img
                  src="../assets/ImageIcon/apidog.png"
                  alt=""
                  class="w-8 h-8 rounded-lg"
                />
                ApiDog
              </span>
            </div>
          </div>
        </div>

        <!-- Payment Gateway -->
        <div class="timeline-container payment-gateway">
          <div class="timeline-icon">
            <i class="fas fa-credit-card"></i>
          </div>
          <div class="timeline-body">
            <h4 class="timeline-title">
              <span class="badge">Payment Gateway</span>
            </h4>
            <div class="skill-tags">
              <span class="skill-tag bakong">
                <img
                  src="../assets/ImageIcon/bakong.png"
                  alt=""
                  class="w-8 h-8 rounded-lg"
                />
                Bakong
              </span>
              <span class="skill-tag stripe">
                <img
                  src="../assets/ImageIcon/stripe.svg"
                  alt=""
                  class="w-8 h-8"
                />
                Stripe
              </span>
            </div>
          </div>
        </div>

        <!-- Database -->
        <div class="timeline-container database">
          <div class="timeline-icon">
            <i class="fas fa-database"></i>
          </div>
          <div class="timeline-body">
            <h4 class="timeline-title">
              <span class="badge">Database</span>
            </h4>
            <div class="skill-tags">
              <span class="skill-tag localstorage">
                <img src="../assets/ImageIcon/storage.svg" alt="" class="w-8 h-8" />
                Local Storage
              </span>
              <span class="skill-tag sqlite">
                <img src="../assets/ImageIcon/sqlite.svg" alt="" class="w-8 h-8" />
                SQLite
              </span>
              <span class="skill-tag hive">
                <img src="../assets/ImageIcon/hive.svg" alt="" class="w-8 h-8" />
                Hive
              </span>
              <span class="skill-tag mysql">
                <img src="../assets/ImageIcon/mysql.svg" alt="" class="w-8 h-8" />
                MySQL
              </span>
              <span class="skill-tag postgresql">
                <img src="../assets/ImageIcon/postgreql.svg" alt="" class="w-8 h-8" />
                PostgreSQL
              </span>
            </div>
          </div>
        </div>
        <!-- Version Control -->
        <div class="timeline-container version-control">
          <div class="timeline-icon">
            <i class="fab fa-git-alt"></i>
          </div>
          <div class="timeline-body">
            <h4 class="timeline-title">
              <span class="badge">Version Control</span>
            </h4>
            <div class="skill-tags">
              <span class="skill-tag git">
                <img src="../assets/ImageIcon/git.svg" alt="" class="w-8 h-8" />
                Git
              </span>
              <span class="skill-tag github">
                <img src="../assets/ImageIcon/github.svg" alt="" class="w-8 h-8" />
                Github
              </span>
              <span class="skill-tag gitlab">
                <img src="../assets/ImageIcon/gitlab.svg" alt="" class="w-8 h-8" />
                Gitlab
              </span>
            </div>
          </div>
        </div>
        <!-- Tools & Utilities -->
        <div class="timeline-container tools">
          <div class="timeline-icon">
            <i class="fas fa-tools"></i>
          </div>
          <div class="timeline-body">
            <h4 class="timeline-title">
              <span class="badge">Tools & Utilities</span>
            </h4>
            <div class="skill-tags">
              <span class="skill-tag vscode">
                <img src="../assets/ImageIcon/vscode.svg" alt="" class="w-8 h-8" />
                Visual Studio Code
              </span>
              <span class="skill-tag android-studio">
                <img src="../assets/ImageIcon/androidstudio.svg" alt="" class="w-8 h-8" />
                Android Studio
              </span>
              <span class="skill-tag docker">
                <img src="../assets/ImageIcon/docker.svg" alt="" class="w-8 h-8" />
                Docker
              </span>
              <span class="skill-tag jenkins">
                <img src="../assets/ImageIcon/jenkins.svg" alt="" class="w-8 h-8" />
                Jenkins
              </span>
              <span class="skill-tag kubernetes">
                <img src="../assets/ImageIcon/k8s.svg" alt="" class="w-8 h-8" />
                Kubernetes
              </span>
              <span class="skill-tag minio">
                <img src="../assets/ImageIcon/minio.svg" alt="" class="w-8 h-8" />
                MinIO
              </span>
              <span class="skill-tag minio">
                <img src="../assets/ImageIcon/dbeaver.svg" alt="" class="w-8 h-8" />
                Dbeaver
              </span>
            </div>
          </div>
        </div>
        <!-- UI/UX Designing Tools -->
        <div class="timeline-container design">
          <div class="timeline-icon">
            <i class="fas fa-palette"></i>
          </div>
          <div class="timeline-body">
            <h4 class="timeline-title">
              <span class="badge">UI/UX Designing Tools</span>
            </h4>
            <div class="skill-tags">
              <span class="skill-tag figma">
                <img src="../assets/ImageIcon/figma.svg" alt="" class="w-8 h-8" />
                Figma
              </span>
              <span class="skill-tag balsamiq">
                <img src="../assets/ImageIcon/balsamiq.png" alt="" class="w-8 h-8" />
                Balsamiq
              </span>
              <span class="skill-tag canva">
                <img src="../assets/ImageIcon/canva.svg" alt="" class="w-8 h-8" />
                Canva
              </span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { onMounted, ref } from "vue";

const isVisible = ref(false);

onMounted(() => {
  // Trigger initial animations
  setTimeout(() => {
    isVisible.value = true;
  }, 100);

  // Add intersection observer for timeline containers
  const observer = new IntersectionObserver(
    (entries) => {
      entries.forEach((entry, index) => {
        if (entry.isIntersecting) {
          // Add staggered animation delays
          setTimeout(() => {
            entry.target.classList.add("animate-in");

            // Animate skill tags within the container
            const skillTags = entry.target.querySelectorAll(".skill-tag");
            skillTags.forEach((tag, tagIndex) => {
              setTimeout(() => {
                tag.classList.add("animate-skill");
              }, tagIndex * 100);
            });
          }, index * 200);
        }
      });
    },
    {
      threshold: 0.3,
      rootMargin: "0px 0px -50px 0px",
    }
  );

  // Observe timeline containers
  setTimeout(() => {
    const containers = document.querySelectorAll(".timeline-container");
    containers.forEach((container) => {
      observer.observe(container);
    });
  }, 500);
});
</script>

<style scoped>
.expertise-container {
  padding: 2rem;
  color: white;
  min-height: 100%;
  overflow-x: hidden;
  background: linear-gradient(
    135deg,
    rgba(15, 23, 42, 0.1) 0%,
    rgba(30, 41, 59, 0.05) 100%
  );
}

/* Header Animations */
.text-center {
  opacity: 0;
  transform: translateY(30px);
  transition: all 0.8s cubic-bezier(0.4, 0, 0.2, 1);
}

.text-center.animate-fade-in {
  opacity: 1;
  transform: translateY(0);
}

.main-title {
  font-size: 4rem;
  font-weight: 800;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 50%, #06b6d4 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  margin-bottom: 1rem;
  text-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
  animation: slideInFromTop 1s ease-out 0.2s both;
  position: relative;
}

.main-title::after {
  content: "";
  position: absolute;
  bottom: -15px;
  left: 50%;
  transform: translateX(-50%);
  width: 0;
  height: 5px;
  background: linear-gradient(90deg, #667eea, #764ba2, #06b6d4);
  border-radius: 3px;
  animation: expandFromCenter 1.5s ease-out 1.5s both;
}

.subtitle {
  font-size: 1.25rem;
  color: #94a3b8;
  font-weight: 400;
  max-width: 600px;
  line-height: 1.6;
  margin: auto;
  animation: slideInFromBottom 1s ease-out 0.6s both;
}

.skill-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
}

.skill-tag {
  display: inline-flex;
  align-items: center;
  gap: 0.75rem;
  padding: 0.75rem 1.25rem;
  background: linear-gradient(
    135deg,
    rgba(99, 102, 241, 0.1) 0%,
    rgba(6, 182, 212, 0.05) 100%
  );
  border: 1px solid rgba(99, 102, 241, 0.2);
  border-radius: 2rem;
  color: #f1f5f9;
  font-size: 0.9rem;
  font-weight: 600;
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  cursor: pointer;
  position: relative;
  overflow: hidden;
  opacity: 0;
  transform: translateY(20px) scale(0.9);
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
}

.skill-tag::before {
  content: "";
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(
    90deg,
    transparent,
    rgba(255, 255, 255, 0.1),
    transparent
  );
  transition: left 0.5s ease;
}

.skill-tag:hover::before {
  left: 100%;
}

.skill-tag.animate-skill {
  opacity: 1;
  transform: translateY(0) scale(1);
  animation: bounceIn 0.6s ease-out both;
}

.skill-tag:hover {
  background: linear-gradient(
    135deg,
    rgba(99, 102, 241, 0.2) 0%,
    rgba(6, 182, 212, 0.15) 100%
  );
  border-color: rgba(6, 182, 212, 0.5);
  transform: translateY(-5px) scale(1.05);
  box-shadow: 0 12px 30px rgba(6, 182, 212, 0.25);
}

/* Enhanced specific skill tag colors with better animations */
.skill-tag.flutter {
  content: "";
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(
    90deg,
    transparent,
    rgba(255, 255, 255, 0.1),
    transparent
  );
  transition: left 0.5s ease;
}

.skill-tag:hover::before {
  left: 100%;
}

.skill-tag:hover {
  background: linear-gradient(
    135deg,
    rgba(99, 102, 241, 0.2) 0%,
    rgba(6, 182, 212, 0.1) 100%
  );
  border-color: rgba(6, 182, 212, 0.5);
  transform: translateY(-3px) scale(1.05);
  box-shadow: 0 8px 25px rgba(6, 182, 212, 0.25);
}

/* Enhanced specific skill tag colors */
.skill-tag.flutter {
  border-color: rgba(2, 136, 209, 0.4);
  background: linear-gradient(
    135deg,
    rgba(2, 136, 209, 0.15) 0%,
    rgba(2, 136, 209, 0.05) 100%
  );
}
.skill-tag.flutter:hover {
  border-color: rgba(2, 136, 209, 0.6);
  box-shadow: 0 8px 25px rgba(2, 136, 209, 0.3);
}

.skill-tag.typescript,
.skill-tag.javascript {
  border-color: rgba(247, 223, 30, 0.4);
  background: linear-gradient(
    135deg,
    rgba(247, 223, 30, 0.15) 0%,
    rgba(247, 223, 30, 0.05) 100%
  );
}
.skill-tag.typescript:hover,
.skill-tag.javascript:hover {
  border-color: rgba(247, 223, 30, 0.6);
  box-shadow: 0 8px 25px rgba(247, 223, 30, 0.3);
}

.skill-tag.riverpod {
  border-color: rgba(78, 205, 196, 0.4);
  background: linear-gradient(
    135deg,
    rgba(78, 205, 196, 0.15) 0%,
    rgba(78, 205, 196, 0.05) 100%
  );
}
.skill-tag.riverpod:hover {
  border-color: rgba(78, 205, 196, 0.6);
  box-shadow: 0 8px 25px rgba(78, 205, 196, 0.3);
}

.skill-tag.pinia {
  border-color: rgba(79, 192, 141, 0.4);
  background: linear-gradient(
    135deg,
    rgba(79, 192, 141, 0.15) 0%,
    rgba(79, 192, 141, 0.05) 100%
  );
}
.skill-tag.pinia:hover {
  border-color: rgba(79, 192, 141, 0.6);
  box-shadow: 0 8px 25px rgba(79, 192, 141, 0.3);
}

.skill-tag.firebase {
  border-color: rgba(255, 193, 7, 0.4);
  background: linear-gradient(
    135deg,
    rgba(255, 193, 7, 0.15) 0%,
    rgba(255, 193, 7, 0.05) 100%
  );
}
.skill-tag.firebase:hover {
  border-color: rgba(255, 193, 7, 0.6);
  box-shadow: 0 8px 25px rgba(255, 193, 7, 0.3);
}

/* API Service colors */
.skill-tag.rest {
  border-color: rgba(92, 184, 92, 0.4);
  background: linear-gradient(
    135deg,
    rgba(92, 184, 92, 0.15) 0%,
    rgba(92, 184, 92, 0.05) 100%
  );
}
.skill-tag.rest:hover {
  border-color: rgba(92, 184, 92, 0.6);
  box-shadow: 0 8px 25px rgba(92, 184, 92, 0.3);
}

.skill-tag.graphql {
  border-color: rgba(233, 30, 99, 0.4);
  background: linear-gradient(
    135deg,
    rgba(233, 30, 99, 0.15) 0%,
    rgba(233, 30, 99, 0.05) 100%
  );
}
.skill-tag.graphql:hover {
  border-color: rgba(233, 30, 99, 0.6);
  box-shadow: 0 8px 25px rgba(233, 30, 99, 0.3);
}

.skill-tag.postman {
  border-color: rgba(255, 111, 43, 0.4);
  background: linear-gradient(
    135deg,
    rgba(255, 111, 43, 0.15) 0%,
    rgba(255, 111, 43, 0.05) 100%
  );
}
.skill-tag.postman:hover {
  border-color: rgba(255, 111, 43, 0.6);
  box-shadow: 0 8px 25px rgba(255, 111, 43, 0.3);
}

.skill-tag.apidog {
  border-color: rgba(76, 175, 80, 0.4);
  background: linear-gradient(
    135deg,
    rgba(76, 175, 80, 0.15) 0%,
    rgba(76, 175, 80, 0.05) 100%
  );
}
.skill-tag.apidog:hover {
  border-color: rgba(76, 175, 80, 0.6);
  box-shadow: 0 8px 25px rgba(76, 175, 80, 0.3);
}

/* Payment Gateway colors */
.skill-tag.bakong {
  border-color: rgba(158, 62, 166, 0.4);
  background: linear-gradient(
    135deg,
    rgba(158, 62, 166, 0.15) 0%,
    rgba(158, 62, 166, 0.05) 100%
  );
}
.skill-tag.bakong:hover {
  border-color: rgba(158, 62, 166, 0.6);
  box-shadow: 0 8px 25px rgba(158, 62, 166, 0.3);
}

.skill-tag.stripe {
  border-color: rgba(108, 99, 255, 0.4);
  background: linear-gradient(
    135deg,
    rgba(108, 99, 255, 0.15) 0%,
    rgba(108, 99, 255, 0.05) 100%
  );
}
.skill-tag.stripe:hover {
  border-color: rgba(108, 99, 255, 0.6);
  box-shadow: 0 8px 25px rgba(108, 99, 255, 0.3);
}

/* Database colors */
.skill-tag.localstorage {
  border-color: rgba(255, 167, 38, 0.4);
  background: linear-gradient(
    135deg,
    rgba(255, 167, 38, 0.15) 0%,
    rgba(255, 167, 38, 0.05) 100%
  );
}
.skill-tag.localstorage:hover {
  border-color: rgba(255, 167, 38, 0.6);
  box-shadow: 0 8px 25px rgba(255, 167, 38, 0.3);
}

.skill-tag.sqlite {
  border-color: rgba(3, 125, 214, 0.4);
  background: linear-gradient(
    135deg,
    rgba(3, 125, 214, 0.15) 0%,
    rgba(3, 125, 214, 0.05) 100%
  );
}
.skill-tag.sqlite:hover {
  border-color: rgba(3, 125, 214, 0.6);
  box-shadow: 0 8px 25px rgba(3, 125, 214, 0.3);
}

.skill-tag.hive {
  border-color: rgba(255, 193, 7, 0.4);
  background: linear-gradient(
    135deg,
    rgba(255, 193, 7, 0.15) 0%,
    rgba(255, 193, 7, 0.05) 100%
  );
}
.skill-tag.hive:hover {
  border-color: rgba(255, 193, 7, 0.6);
  box-shadow: 0 8px 25px rgba(255, 193, 7, 0.3);
}

.skill-tag.mysql {
  border-color: rgba(0, 117, 143, 0.4);
  background: linear-gradient(
    135deg,
    rgba(0, 117, 143, 0.15) 0%,
    rgba(0, 117, 143, 0.05) 100%
  );
}
.skill-tag.mysql:hover {
  border-color: rgba(0, 117, 143, 0.6);
  box-shadow: 0 8px 25px rgba(0, 117, 143, 0.3);
}

.skill-tag.postgresql {
  border-color: rgba(51, 103, 145, 0.4);
  background: linear-gradient(
    135deg,
    rgba(51, 103, 145, 0.15) 0%,
    rgba(51, 103, 145, 0.05) 100%
  );
}
.skill-tag.postgresql:hover {
  border-color: rgba(51, 103, 145, 0.6);
  box-shadow: 0 8px 25px rgba(51, 103, 145, 0.3);
}

/* Version Control colors */
.skill-tag.git {
  border-color: rgba(240, 80, 51, 0.4);
  background: linear-gradient(
    135deg,
    rgba(240, 80, 51, 0.15) 0%,
    rgba(240, 80, 51, 0.05) 100%
  );
}
.skill-tag.git:hover {
  border-color: rgba(240, 80, 51, 0.6);
  box-shadow: 0 8px 25px rgba(240, 80, 51, 0.3);
}

.skill-tag.github {
  border-color: rgba(23, 122, 221, 0.4);
  background: linear-gradient(
    135deg,
    rgba(36, 41, 46, 0.15) 0%,
    rgba(36, 41, 46, 0.05) 100%
  );
}
.skill-tag.github:hover {
  border-color: rgba(120, 120, 120, 0.6);
  box-shadow: 0 8px 25px rgba(120, 120, 120, 0.3);
}

.skill-tag.gitlab {
  border-color: rgba(252, 109, 38, 0.4);
  background: linear-gradient(
    135deg,
    rgba(252, 109, 38, 0.15) 0%,
    rgba(252, 109, 38, 0.05) 100%
  );
}
.skill-tag.gitlab:hover {
  border-color: rgba(252, 109, 38, 0.6);
  box-shadow: 0 8px 25px rgba(252, 109, 38, 0.3);
}

/* Tools & Utilities colors */
.skill-tag.vscode {
  border-color: rgba(37, 150, 190, 0.4);
  background: linear-gradient(
    135deg,
    rgba(37, 150, 190, 0.15) 0%,
    rgba(37, 150, 190, 0.05) 100%
  );
}
.skill-tag.vscode:hover {
  border-color: rgba(37, 150, 190, 0.6);
  box-shadow: 0 8px 25px rgba(37, 150, 190, 0.3);
}

.skill-tag.android-studio {
  border-color: rgba(59, 180, 74, 0.4);
  background: linear-gradient(
    135deg,
    rgba(59, 180, 74, 0.15) 0%,
    rgba(59, 180, 74, 0.05) 100%
  );
}
.skill-tag.android-studio:hover {
  border-color: rgba(59, 180, 74, 0.6);
  box-shadow: 0 8px 25px rgba(59, 180, 74, 0.3);
}

.skill-tag.docker {
  border-color: rgba(13, 183, 237, 0.4);
  background: linear-gradient(
    135deg,
    rgba(13, 183, 237, 0.15) 0%,
    rgba(13, 183, 237, 0.05) 100%
  );
}
.skill-tag.docker:hover {
  border-color: rgba(13, 183, 237, 0.6);
  box-shadow: 0 8px 25px rgba(13, 183, 237, 0.3);
}

.skill-tag.jenkins {
  border-color: rgba(213, 70, 52, 0.4);
  background: linear-gradient(
    135deg,
    rgba(213, 70, 52, 0.15) 0%,
    rgba(213, 70, 52, 0.05) 100%
  );
}
.skill-tag.jenkins:hover {
  border-color: rgba(213, 70, 52, 0.6);
  box-shadow: 0 8px 25px rgba(213, 70, 52, 0.3);
}

.skill-tag.kubernetes {
  border-color: rgba(50, 108, 229, 0.4);
  background: linear-gradient(
    135deg,
    rgba(50, 108, 229, 0.15) 0%,
    rgba(50, 108, 229, 0.05) 100%
  );
}
.skill-tag.kubernetes:hover {
  border-color: rgba(50, 108, 229, 0.6);
  box-shadow: 0 8px 25px rgba(50, 108, 229, 0.3);
}

.skill-tag.minio {
  border-color: rgba(199, 49, 122, 0.4);
  background: linear-gradient(
    135deg,
    rgba(199, 49, 122, 0.15) 0%,
    rgba(199, 49, 122, 0.05) 100%
  );
}
.skill-tag.minio:hover {
  border-color: rgba(199, 49, 122, 0.6);
  box-shadow: 0 8px 25px rgba(199, 49, 122, 0.3);
}

/* UI/UX Designing Tools colors */
.skill-tag.figma {
  border-color: rgba(162, 89, 255, 0.4);
  background: linear-gradient(
    135deg,
    rgba(162, 89, 255, 0.15) 0%,
    rgba(162, 89, 255, 0.05) 100%
  );
}
.skill-tag.figma:hover {
  border-color: rgba(162, 89, 255, 0.6);
  box-shadow: 0 8px 25px rgba(162, 89, 255, 0.3);
}

.skill-tag.balsamiq {
  border-color: rgba(204, 51, 51, 0.4);
  background: linear-gradient(
    135deg,
    rgba(204, 51, 51, 0.15) 0%,
    rgba(204, 51, 51, 0.05) 100%
  );
}
.skill-tag.balsamiq:hover {
  border-color: rgba(204, 51, 51, 0.6);
  box-shadow: 0 8px 25px rgba(204, 51, 51, 0.3);
}

.skill-tag.canva {
  border-color: rgba(133, 213, 255, 0.4);
  background: linear-gradient(
    135deg,
    rgba(133, 213, 255, 0.15) 0%,
    rgba(133, 213, 255, 0.05) 100%
  );
}
.skill-tag.canva:hover {
  border-color: rgba(133, 213, 255, 0.6);
  box-shadow: 0 8px 25px rgba(133, 213, 255, 0.3);
}

/* Additional skill tag colors for new technologies */
.skill-tag.html {
  border-color: rgba(227, 76, 38, 0.4);
  background: linear-gradient(
    135deg,
    rgba(227, 76, 38, 0.15) 0%,
    rgba(227, 76, 38, 0.05) 100%
  );
}
.skill-tag.html:hover {
  border-color: rgba(227, 76, 38, 0.6);
  box-shadow: 0 8px 25px rgba(227, 76, 38, 0.3);
}

.skill-tag.css {
  border-color: rgba(21, 114, 182, 0.4);
  background: linear-gradient(
    135deg,
    rgba(21, 114, 182, 0.15) 0%,
    rgba(21, 114, 182, 0.05) 100%
  );
}
.skill-tag.css:hover {
  border-color: rgba(21, 114, 182, 0.6);
  box-shadow: 0 8px 25px rgba(21, 114, 182, 0.3);
}

.skill-tag.python {
  border-color: rgba(55, 118, 171, 0.4);
  background: linear-gradient(
    135deg,
    rgba(55, 118, 171, 0.15) 0%,
    rgba(55, 118, 171, 0.05) 100%
  );
}
.skill-tag.python:hover {
  border-color: rgba(55, 118, 171, 0.6);
  box-shadow: 0 8px 25px rgba(55, 118, 171, 0.3);
}

.skill-tag.vuejs {
  border-color: rgba(79, 192, 141, 0.4);
  background: linear-gradient(
    135deg,
    rgba(79, 192, 141, 0.15) 0%,
    rgba(79, 192, 141, 0.05) 100%
  );
}
.skill-tag.vuejs:hover {
  border-color: rgba(79, 192, 141, 0.6);
  box-shadow: 0 8px 25px rgba(79, 192, 141, 0.3);
}

.skill-tag.laravel {
  border-color: rgba(255, 45, 32, 0.4);
  background: linear-gradient(
    135deg,
    rgba(255, 45, 32, 0.15) 0%,
    rgba(255, 45, 32, 0.05) 100%
  );
}
.skill-tag.laravel:hover {
  border-color: rgba(255, 45, 32, 0.6);
  box-shadow: 0 8px 25px rgba(255, 45, 32, 0.3);
}

.skill-tag.nestjs {
  border-color: rgba(234, 20, 79, 0.4);
  background: linear-gradient(
    135deg,
    rgba(234, 20, 79, 0.15) 0%,
    rgba(234, 20, 79, 0.05) 100%
  );
}
.skill-tag.nestjs:hover {
  border-color: rgba(234, 20, 79, 0.6);
  box-shadow: 0 8px 25px rgba(234, 20, 79, 0.3);
}

.skill-tag.tailwindcss {
  border-color: rgba(56, 178, 172, 0.4);
  background: linear-gradient(
    135deg,
    rgba(56, 178, 172, 0.15) 0%,
    rgba(56, 178, 172, 0.05) 100%
  );
}
.skill-tag.tailwindcss:hover {
  border-color: rgba(56, 178, 172, 0.6);
  box-shadow: 0 8px 25px rgba(56, 178, 172, 0.3);
}

.skill-tag.java {
  border-color: rgba(237, 117, 36, 0.4);
  background: linear-gradient(
    135deg,
    rgba(237, 117, 36, 0.15) 0%,
    rgba(237, 117, 36, 0.05) 100%
  );
}
.skill-tag.java:hover {
  border-color: rgba(237, 117, 36, 0.6);
  box-shadow: 0 8px 25px rgba(237, 117, 36, 0.3);
}

.skill-tag.c {
  border-color: rgba(92, 107, 192, 0.4);
  background: linear-gradient(
    135deg,
    rgba(92, 107, 192, 0.15) 0%,
    rgba(92, 107, 192, 0.05) 100%
  );
}
.skill-tag.c:hover {
  border-color: rgba(92, 107, 192, 0.6);
  box-shadow: 0 8px 25px rgba(92, 107, 192, 0.3);
}

.skill-tag.cpp {
  border-color: rgba(0, 89, 156, 0.4);
  background: linear-gradient(
    135deg,
    rgba(0, 89, 156, 0.15) 0%,
    rgba(0, 89, 156, 0.05) 100%
  );
}
.skill-tag.cpp:hover {
  border-color: rgba(0, 89, 156, 0.6);
  box-shadow: 0 8px 25px rgba(0, 89, 156, 0.3);
}

/* Timeline Styles */
.timeline {
  position: relative;
  padding-left: 4rem;
  margin: 0 0 0 30px;
  color: white;
}

.timeline:before {
  content: "";
  position: absolute;
  left: 0;
  top: 0;
  width: 4px;
  height: 100%;
  background: linear-gradient(
    180deg,
    #ff6b6b 0%,
    #4ecdc4 14%,
    #f093fb 28%,
    #ffa726 42%,
    #66bb6a 56%,
    #9c27b0 70%,
    #607d8b 84%,
    #e91e63 100%
  );
  border-radius: 2px;
  box-shadow: 0 0 20px rgba(255, 107, 107, 0.3);
  animation: timelineGlow 4s ease-in-out infinite alternate;
}

.timeline-container {
  position: relative;
  margin-bottom: 2.5rem;
}

.timeline-icon {
  position: absolute;
  left: -72px;
  top: 60px;
  width: 20px;
  height: 20px;
  border-radius: 100%;
  text-align: center;
  font-size: 1.5rem;
  background: #4f537b;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.3);
  transition: all 0.3s ease;
  border: 3px solid #1a1a2e;
}

.timeline-body {
  background: linear-gradient(
    145deg,
    rgba(39, 41, 61, 0.95) 0%,
    rgba(39, 41, 61, 0.8) 100%
  );
  backdrop-filter: blur(15px);
  border-radius: 12px;
  padding: 20px 20px 15px;
  margin-top: 20px;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
  border: 1px solid rgba(255, 255, 255, 0.1);
  position: relative;
  transition: all 0.3s ease;
}

.timeline-body:before {
  content: "";
  background: inherit;
  width: 20px;
  height: 20px;
  display: block;
  position: absolute;
  left: -10px;
  top: 15px;
  transform: rotate(45deg);
  border-radius: 0 0 0 2px;
  border-left: 1px solid rgba(255, 255, 255, 0.1);
  border-bottom: 1px solid rgba(255, 255, 255, 0.1);
}

.timeline-container:hover .timeline-body {
  background: linear-gradient(
    145deg,
    rgba(39, 41, 61, 1) 0%,
    rgba(39, 41, 61, 0.9) 100%
  );
  transform: translateY(-2px);
  box-shadow: 0 12px 40px rgba(0, 0, 0, 0.4);
}

.timeline-container:hover .timeline-icon {
  transform: scale(1.1);
  box-shadow: 0 6px 25px rgba(0, 0, 0, 0.4);
}

.timeline-title {
  margin-bottom: 1.4rem;
  font-size: 1.1rem;
}

.timeline-title .badge {
  background: #4f537b;
  padding: 6px 12px;
  border-radius: 6px;
  font-size: 14px;
  font-weight: bold;
  color: white;
  border: 1px solid rgba(255, 255, 255, 0.2);
}

/* Timeline container specific colors */
.timeline-container.frameworks .timeline-icon,
.timeline-container.frameworks .badge {
  background: linear-gradient(135deg, #ff6b6b 0%, #ff8e8e 100%) !important;
  box-shadow: 0 4px 15px rgba(255, 107, 107, 0.4);
}

.timeline-container.state-management .timeline-icon,
.timeline-container.state-management .badge {
  background: linear-gradient(135deg, #4ecdc4 0%, #44a08d 100%) !important;
  box-shadow: 0 4px 15px rgba(78, 205, 196, 0.4);
}

.timeline-container.plugins .timeline-icon,
.timeline-container.plugins .badge {
  background: linear-gradient(135deg, #45b7d1 0%, #96c93d 100%) !important;
  box-shadow: 0 4px 15px rgba(69, 183, 209, 0.4);
}

.timeline-container.api-service .timeline-icon,
.timeline-container.api-service .badge {
  background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%) !important;
  box-shadow: 0 4px 15px rgba(240, 147, 251, 0.4);
}

.timeline-container.payment-gateway .timeline-icon,
.timeline-container.payment-gateway .badge {
  background: linear-gradient(135deg, #ffa726 0%, #fb8c00 100%) !important;
  box-shadow: 0 4px 15px rgba(255, 167, 38, 0.4);
}

.timeline-container.database .timeline-icon,
.timeline-container.database .badge {
  background: linear-gradient(135deg, #66bb6a 0%, #43a047 100%) !important;
  box-shadow: 0 4px 15px rgba(102, 187, 106, 0.4);
}

.timeline-container.version-control .timeline-icon,
.timeline-container.version-control .badge {
  background: linear-gradient(135deg, #9c27b0 0%, #673ab7 100%) !important;
  box-shadow: 0 4px 15px rgba(156, 39, 176, 0.4);
}

.timeline-container.tools .timeline-icon,
.timeline-container.tools .badge {
  background: linear-gradient(135deg, #607d8b 0%, #455a64 100%) !important;
  box-shadow: 0 4px 15px rgba(96, 125, 139, 0.4);
}

.timeline-container.design .timeline-icon,
.timeline-container.design .badge {
  background: linear-gradient(135deg, #e91e63 0%, #ad1457 100%) !important;
  box-shadow: 0 4px 15px rgba(233, 30, 99, 0.4);
}

@media (max-width: 768px) {
  .expertise-container {
    padding: 1rem;
  }

  .skill-tags {
    justify-content: center;
  }

  /* Responsive timeline adjustments */
  .timeline {
    padding-left: 3rem;
    margin: 0 0 0 20px;
  }

  .timeline-icon {
    left: -65px;
    width: 40px;
    height: 40px;
    font-size: 1.2rem;
  }

  .timeline-body {
    padding: 15px;
  }

  .timeline-body:before {
    width: 15px;
    height: 15px;
    left: -7px;
  }

  .timeline-title .badge {
    font-size: 12px;
    padding: 4px 8px;
  }
}

/* Enhanced timeline animations and effects */
.timeline-container {
  position: relative;
  margin-bottom: 2.5rem;
  opacity: 0;
  transform: translateX(-50px);
  transition: all 0.6s cubic-bezier(0.4, 0, 0.2, 1);
}

.timeline-container.animate-in {
  opacity: 1;
  transform: translateX(0);
}

.timeline-body {
  position: relative;
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  overflow: hidden;
}

.timeline-body::after {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 3px;
  background: linear-gradient(
    90deg,
    transparent,
    rgba(99, 102, 241, 0.5),
    transparent
  );
  opacity: 0;
  transition: opacity 0.3s ease;
}

.timeline-container:hover .timeline-body::after {
  opacity: 1;
}

.timeline-container:hover .timeline-body {
  transform: translateY(-3px) scale(1.01);
  box-shadow: 0 15px 40px rgba(0, 0, 0, 0.3);
}

.timeline-icon {
  position: relative;
  overflow: hidden;
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
}

.timeline-icon::before {
  content: "";
  position: absolute;
  top: 50%;
  left: 50%;
  width: 0;
  height: 0;
  background: rgba(255, 255, 255, 0.3);
  border-radius: 50%;
  transform: translate(-50%, -50%);
  transition: all 0.4s ease;
}

.timeline-container:hover .timeline-icon::before {
  width: 100%;
  height: 100%;
}

.timeline-container:hover .timeline-icon {
  transform: scale(1.15) rotate(5deg);
  box-shadow: 0 12px 35px rgba(0, 0, 0, 0.4);
}

/* Keyframe Animations */
@keyframes slideInFromTop {
  from {
    opacity: 0;
    transform: translateY(-50px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes slideInFromBottom {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes expandFromCenter {
  from {
    width: 0;
  }
  to {
    width: 150px;
  }
}

@keyframes bounceIn {
  0% {
    opacity: 0;
    transform: translateY(20px) scale(0.3);
  }
  50% {
    opacity: 1;
    transform: translateY(-5px) scale(1.05);
  }
  70% {
    transform: translateY(2px) scale(0.95);
  }
  100% {
    opacity: 1;
    transform: translateY(0) scale(1);
  }
}

@keyframes timelineGlow {
  0% {
    box-shadow: 0 0 20px rgba(255, 107, 107, 0.3);
  }
  25% {
    box-shadow: 0 0 25px rgba(78, 205, 196, 0.4);
  }
  50% {
    box-shadow: 0 0 30px rgba(69, 183, 209, 0.5);
  }
  75% {
    box-shadow: 0 0 25px rgba(150, 201, 61, 0.4);
  }
  100% {
    box-shadow: 0 0 20px rgba(255, 107, 107, 0.3);
  }
}

/* Reduced motion accessibility */
@media (prefers-reduced-motion: reduce) {
  .timeline-container,
  .timeline-icon,
  .timeline-body,
  .skill-tag,
  .text-center {
    transition: none;
    animation: none;
  }

  .timeline-container,
  .skill-tag,
  .text-center {
    opacity: 1;
    transform: none;
  }

  .timeline:before {
    animation: none;
  }
}
</style>
