<template>
  <div class="relative">
    <div class="carousel-wrapper">
      <div class="carousel-inner">
        <div
          v-for="(project, index) in projects"
          :key="project.id"
          class="carousel-item"
          :class="{ active: index === currentIndex }"
        >
          <ProjectCard :project="project" />
        </div>
      </div>
    </div>
    <div class="carousel-controls absolute bottom-0 left-0 right-0">
      <div class="container mx-auto px-6 flex justify-center items-center">
        <button
          class="carousel-control mr-4"
          :disabled="currentIndex === 0"
          @click="prev"
        >
          <span class="sr-only">Previous</span>
          <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" viewBox="0 0 20 20" fill="currentColor">
            <path fill-rule="evenodd" d="M13.707 4.293a1 1 0 011.414 0l3 3a1 1 0 010 1.414l-3 3a1 1 0 01-1.414-1.414L14.586 9H3a1 1 0 110-2h11.586l-1.293-1.293a1 1 0 010-1.414z" clip-rule="evenodd" />
          </svg>
        </button>
        <button
          class="carousel-control"
          :disabled="currentIndex === projects.length - 1"
          @click="next"
        >
          <span class="sr-only">Next</span>
          <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" viewBox="0 0 20 20" fill="currentColor">
            <path fill-rule="evenodd" d="M6.293 15.707a1 1 0 01-1.414 0l-3-3a1 1 0 010-1.414l3-3a1 1 0 111.414 1.414L5.414 11H17a1 1 0 110 2H5.414l1.293 1.293a1 1 0 010 1.414z" clip-rule="evenodd" />
          </svg>
        </button>
      </div>
    </div>
  </div>
</template>

<script>
import ProjectCard from '~/components/ProjectCard.vue';
import projectsData from '~/data/projects.json';

export default {
  components: {
    ProjectCard,
  },
  data() {
    return {
      currentIndex: 0,
      projects: projectsData,
    };
  },
  methods: {
    next() {
      this.currentIndex = Math.min(
        this.currentIndex + 1,
        this.projects.length - 1
      );
    },
    prev() {
      this.currentIndex = Math.max(this.currentIndex - 1, 0);
    },
  },
};
</script>
