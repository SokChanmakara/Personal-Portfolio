<script setup>
defineProps({
  name: {
    type: String,
    default: "SOK CHANMAKARA",
  },
  title: {
    type: String,
    default: "SOFTWARE DEVELOPER",
  },
  profileImage: {
    type: String,
    default:
      "https://i.pinimg.com/736x/cf/d1/df/cfd1df905cde736fc5bf7704de635d7b.jpg",
  },
  altText: {
    type: String,
    default: "Profile picture",
  },
});
</script>

<template>
  <div class="sidebar">
    <div class="profile">
      <div class="image">
        <img :src="profileImage" :alt="altText" />
      </div>
      <div class="name-container">
        <div class="name">
          <p>{{ name }}</p>
        </div>
        <div class="title">
          <p>{{ title }}</p>
        </div>
      </div>
    </div>
    <div class="sidebar-info">
      <slot name="sidebar-content" />
    </div>
  </div>
</template>

<style scoped>
.sidebar {
  width: 100%;
  max-width: 275px;
  min-width: 250px;
  height: auto;
  min-height: 600px;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  padding: 20px;
  border: 1px solid #514f4f;
  border-radius: 30px;
  background-color: var(--color-background);
  flex: 0 0 auto;
}

.profile {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  width: 100%;
}

.name-container {
  padding: 20px;
}

.name p {
  font-size: larger;
  font-weight: bold;
  color: white;
  margin: 0 0 10px 0;
}

.title {
  font-size:smaller;
  position: relative;
}

.title::after {
  content: "";
  position: absolute;
  bottom: -25px;
  left: 50%;
  transform: translateX(-50%);
  width: 220px;
  height: 2px;
  background-color: var(--vt-c-indigo);
  border-radius: 1px;
}

.title p {
  margin: 0;
  padding: 6px;
  border-radius: 12px;
  color: white;
  background-color: rgb(41, 41, 43);
}

.image img {
  height: 150px;
  width: 150px;
  border-radius: 20px;
  object-fit: cover;
}

.sidebar-info {
  flex: 1;
  margin-top: 30px;
}

/* Responsive breakpoints */
@media (max-width: 768px) {
  .sidebar {
    max-width: 100%;
  }

  .image img {
    height: 120px;
    width: 120px;
  }
}

@media (max-width: 480px) {
  .sidebar {
    padding: 15px;
  }

  .name-container {
    padding: 15px;
  }

  .image img {
    height: 100px;
    width: 100px;
  }
}
</style>
