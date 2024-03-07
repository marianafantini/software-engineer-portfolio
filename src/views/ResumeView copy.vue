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

    <div class="content">
      <div class="work-experience">
        <h3>Work experience</h3>
        <div class="items">
          <div v-for="work in workItems" class="item" :key="work">
            <div>{{ work.initialDate }} - {{ work.endDate }}</div>
            <div class="info">
              <div class="title">{{ work.position }}</div>
              <div class="place">{{ work.company }}</div>
            </div>
          </div>
        </div>
      </div>
      <div class="education-history">
        <h3>Education</h3>
        <div class="items">
          <div v-for="school in schoolItems" class="item" :key="school">
            <div>{{ school.initialDate }} - {{ school.endDate }}</div>
            <div class="info">
              <div class="title">{{ school.course }}</div>
              <div class="place">{{ school.university }}</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.resume {
  padding: 1rem 0;
  text-align: center;
}
.content {
  display: flex;
  padding-right: 2rem;
  .work-experience, .education-history {
    width: 50%;
  }
}
.grid {
  padding: 1rem 0;
  display: grid;
  row-gap: 2rem;
  grid-template-columns: repeat(auto-fill, minmax(400px, 1fr));

  a {
    color: var(--medium-brown);
  }
}
.items {
  display: grid;
  row-gap: 1rem;

  .item {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));

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
</style>
