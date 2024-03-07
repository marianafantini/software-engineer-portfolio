<script setup>
import { RouterView } from 'vue-router';
import PresentationComponent from './components/PresentationComponent.vue';
import { LeftOutlined } from '@ant-design/icons-vue';

const isNotInHome = (currentPath) => {
  console.log(currentPath);
  return currentPath !== 'home';
};
</script>

<template>
  <header></header>
  <div class="content">
    <div class="presentation-wrapper">
      <PresentationComponent />
    </div>

    <div class="router-wrapper">
      <RouterLink class="home-link" to="/" v-if="isNotInHome($route?.name)">
        <LeftOutlined /> Home
      </RouterLink>

      <RouterView />
    </div>
  </div>
</template>

<style scoped>
.content {
  display: grid;
  width: 100%;
  grid-auto-flow: column;
  align-items: center;
}
.presentation-wrapper,
.router-wrapper {
  height: 100%;
  width: 100%;
}
.presentation-wrapper {
  width: 35vw;
  background-color: var(--medium-brown);
  color: var(--light-beige);
}
.router-wrapper {
  width: 63vw;
}
.home-link {
  color: var(--medium-brown);
  padding: 1rem;
}
@media (max-width: 1024px) {
  .content {
    display: flex;
    flex-direction: column;
    width: 100vw;
  }
  .presentation-wrapper,
  .router-wrapper {
    height: 100%;
    width: 100vw;
  }
}
</style>
