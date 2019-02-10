<template>
  <div class="projects-container" id="projects">
    <div class="projects-header-container">
      <h2 class="projects-header">Projects</h2>
    </div>
    <div class="projects-grid">
      <Card
        v-for="project in projects"
        :key="project.title"
        :project="project"
      />
    </div>
  </div>
</template>

<script>
import Card from './Card';

export default {
  name: 'Projects',
  components: { Card },
  data() {
    return {
      projects: [
        {
          title: 'Pickleheads Club',
          description: 'This website',
          image: '/img/projects/pickleheads.jpg',
          actions: [
            {
              name: 'GitHub',
              url: 'https://github.com/pickleheads/pickleheads',
            },
          ],
        },
        {
          title: 'Pickle Jar CLI',
          description: 'A CLI for the place to store all of our ideas',
          image: '/img/projects/pickle-jar-cli.jpg',
          actions: [
            {
              name: 'GitHub',
              url: 'https://github.com/pickleheads/pickle-jar-cli',
            },
          ],
        },
        {
          title: 'Pickle Jar API',
          description: 'An API for the place to store all of our ideas',
          image: '/img/projects/pickle-jar-cli.jpg',
          actions: [
            {
              name: 'GitHub',
              url: 'https://github.com/pickleheads/pickle-jar-api',
            },
          ],
        },
        {
          title: 'Pickle Jar Mobile Client',
          description: 'A mobile app to access our shitty ideas',
          image: '/img/projects/pickle-jar-cli.jpg',
          actions: [
            {
              name: 'GitHub',
              url: 'https://github.com/pickleheads/pickle-jar-mobile-app',
            },
          ],
        },
      ],
    };
  },
};
</script>

<style scoped>
.projects-container {
  min-height: calc(100vh - 80px);
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 40px 40px;
}

@media (max-width: 576px) {
  .projects-container {
    padding: 40px 10px;
  }
}

.projects-header {
  margin-bottom: 40px;
}

.projects-header-container {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  grid-gap: 40px;
  max-width: 800px;
  width: 100%;
}
</style>
