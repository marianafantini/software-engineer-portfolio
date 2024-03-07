<script setup>
const schoolItems = [
  {
    university: 'Universidade Estadual Paulista Júlio de Mesquita Filho - UNESP',
    city: 'Rio Claro, Brazil',
    course: 'Bachelors in Computer Science',
    initialDate: '2013-03',
    endDate: '2017-12',
  },
  {
    university: 'Heriot Watt University',
    city: 'Edinburgh, Scotland',
    course: 'Bachelors in Computer Science',
    initialDate: '2015-09',
    endDate: '2016-06',
  },
];

const workItems = [
  {
    company: 'Nubank',
    city: 'São Paulo, São Paulo Brazil',
    position: 'Senior Software Engineer',
    initialDate: '2021-09',
    endDate: 'current',
  },
  {
    company: 'Nubank',
    city: 'São Paulo, São Paulo Brazil',
    position: 'Software Engineer',
    initialDate: '2020-01',
    endDate: '2021-09',
  },
  {
    company: 'Wavy',
    city: 'Campinas, São Paulo, Brazil',
    position: 'Associate Software Engineer',
    initialDate: '2018-01',
    endDate: '2019-12',
  },
];
</script>

<template>
  <div class="resume">
    <h2 class="ibm-plex-mono-medium">Resume</h2>
    <h3 class="ibm-plex-mono-medium">About me</h3>
    <p class="roboto-mono text">
      As a full-stack developer with over 6 years of industry experience, I enjoy solving complex
      problems and crafting direct, user-friendly interfaces. My journey has led me through diverse
      projects, from backend architecture to pixel-perfect frontend design.
    </p>
    <hr />
    <h3 class="ibm-plex-mono-medium">Work experience</h3>
    <div class="items">
      <div v-for="work in workItems" class="item" :key="work">
        <div class="text">{{ work.initialDate }} - {{ work.endDate }}</div>
        <div class="info">
          <div class="title text">{{ work.position }}</div>
          <div class="place text">{{ work.company }}</div>
        </div>
      </div>
    </div>
    <hr />
    <h3 class="ibm-plex-mono-medium">Education</h3>
    <div class="items">
      <div v-for="school in schoolItems" class="item" :key="school">
        <div class="text">{{ school.initialDate }} - {{ school.endDate }}</div>
        <div class="info">
          <div class="title text">{{ school.course }}</div>
          <div class="place text">{{ school.university }}</div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.resume {
  padding: 1rem 2rem;
  h2 {
    text-align: center;
  }
}
.items {
  display: grid;
  row-gap: 1rem;

  .item {
    display: grid;
    grid-template-columns: 10rem 1fr;

    .info {
      text-align: start;
    }
    .title {
      font-weight: 600;
    }
    .place {
      font-size: 0.8rem;
    }
  }
}
.text {
  font-size: 0.7rem;
}
hr {
  border-top: 1px solid var(--light-brown);
}
</style>
