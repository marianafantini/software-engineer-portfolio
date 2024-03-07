<script setup></script>

<template>
  <div class="portfolio">
    <h2 class="ibm-plex-mono-medium">Previous work</h2>
    <div class="grid">
      <a target="_blank" href="https://marianafantini.github.io/dog-ngo-canva-website/">
        <img src="/assets/portfolio-ngo.png" height="200" />
        <p>Project of website to Dog's NGO</p>
      </a>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.portfolio {
  padding: 1rem 0;
  text-align: center;
}
.grid {
  padding-top: 1rem;
  display: grid;
  row-gap: 2rem;
  grid-template-columns: repeat(auto-fill, minmax(400px, 1fr));

  a {
    color: var(--medium-brown);
  }
}
@media (max-width: 1024px) {
  .grid {
    grid-template-columns: auto;
  }
}
</style>
