<script setup>
import { RouterLink } from 'vue-router';
</script>

<template>
  <main class="about">
    <div class="about-text">
      <h2 class="ibm-plex-mono-medium">{{ '< / About >' }}</h2>
      <p class="roboto-mono">
        As a full-stack developer with over 6 years of industry experience, I enjoy solving complex
        problems and crafting direct, user-friendly interfaces. My journey has led me through
        diverse projects, from backend architecture to pixel-perfect frontend design.
      </p>
    </div>
    <div class="buttons">
      <RouterLink to="/resume"> <button>Resume</button> </RouterLink>
      <RouterLink to="/portfolio"> <button>Portfolio</button> </RouterLink>
    </div>
  </main>
</template>

<style lang="scss" scoped>
.about {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-evenly;
  height: 100vh;
  > .about-text {
    max-width: 50%;
    text-align: center;
  }
  h2 {
    font-size: 2.5rem;
  }
}
.buttons {
  display: flex;
  width: 100%;
  justify-content: space-evenly;
  button {
    cursor: pointer;
  }
}
</style>
