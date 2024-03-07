<script setup>
import { MailFilled, GithubFilled, LinkedinFilled } from '@ant-design/icons-vue';
</script>

<template>
  <div class="presentation">
    <div class="name-and-image">
      <img src="/assets/foto-rosto-MarianaFantini.jpeg" height="300px" />
      <h1 class="ibm-plex-mono-medium name">{{ 'Mariana Fantini' }}</h1>
      <h3 class="roboto-mono position">Software Engineer (she/her)</h3>
    </div>
    <div class="contact">
      <a href="mailto:mariana.fantini.dev@gmail.com">
        <MailFilled :style="{ fontSize: '2rem' }" />
      </a>
      <a target="_blank" href="https://github.com/marianafantini">
        <GithubFilled :style="{ fontSize: '2rem' }" />
      </a>
      <a target="_blank" href="https://www.linkedin.com/in/marianafantini/">
        <LinkedinFilled :style="{ fontSize: '2rem' }" />
      </a>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.presentation {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-evenly;
  height: 100vh;

  .name-and-image {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-evenly;
  }
}
img {
  border-radius: 0.5rem;
}
.position {
  font-weight: 300;
}
h1 {
  margin-bottom: 0;
}
h3 {
  margin-top: 0;
}
.contact {
  display: flex;
  justify-content: space-between;
  width: 7rem;
}
</style>
