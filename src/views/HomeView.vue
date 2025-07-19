<script setup>
import ProfileCard from "../components/ProfileCard.vue";
import MainContent from "../components/MainContent.vue";
</script>

<template>
  <div class="container">
    <ProfileCard
      name="SOK CHANMAKARA"
      title="SOFTWARE DEVELOPER"
      profile-image="https://i.pinimg.com/736x/cf/d1/df/cfd1df905cde736fc5bf7704de635d7b.jpg"
      alt-text="Profile picture"
    >
      <template #sidebar-content>
        <!-- Add additional sidebar content here -->
        <!-- For example: contact info, skills, social links, etc. -->
      </template>
    </ProfileCard>

    <MainContent>
      <!-- Add main content here -->
      <!-- For example: portfolio projects, about section, etc. -->
    </MainContent>
  </div>
</template>

<style scoped>
.container {
  display: flex;
  gap: 20px;
  margin: 10px;
  flex-wrap: wrap;
}

/* Responsive breakpoints */
@media (max-width: 768px) {
  .container {
    flex-direction: column;
  }
}
</style>
