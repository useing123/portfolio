<template>
  <div>
    <ProjectDetails v-for="project in projects" :key="project.id" :project="project" />
  </div>
</template>

<script>
import { projects } from '~/data/projects.js';
import ProjectDetails from '~/components/ProjectCard.vue';

export default {
  components: {
    ProjectDetails,
  },
  data() {
    return {
      projects: projects,
    };
  },
};
</script>
