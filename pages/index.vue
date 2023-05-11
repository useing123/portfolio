<template>
  <div>
    <Header />
    <div class="container mx-auto px-4 py-8">
      <h1 class="text-4xl text-gray-900 mb-8">Дизайн - это не только как выглядит продукт, но и как он работает.
        - Jobs, Steve</h1>
      <h2 class="text-4xl font-bold text-gray-900 mb-8">Мои проекты</h2>
      <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-8">
        <ProjectCard v-for="project in projects" :key="project.id" :project="project" />
      </div>
      <h2 class="text-2xl font-bold text-gray-900 mt-16 mb-8">
        Напишите мне
      </h2>
      <ContactForm />
    </div>
    <Footer />
  </div>
</template>

<script>
import { projects } from '~/data/projects';
import Header from '~/components/Header.vue';
import Footer from '~/components/Footer.vue';
import ContactForm from '~/components/ContactForm.vue';
import ProjectCard from '~/components/ProjectCard.vue';

export default {
  components: {
    Header,
    Footer,
    ContactForm,
    ProjectCard,
  },
  data() {
    return {
      projects,
    };
  },
};
</script>

<style lang="css">
.container {
  max-width: 1140px;
  margin-top: 80px
}

.text-gray-900 {
  color: #1a202c;
}

.text-indigo-600 {
  color: #4f46e5;
}

.bg-indigo-600 {
  background-color: #4f46e5;
}

.hover\:bg-indigo-700:hover {
  background-color: #4338ca;
}

.text-white {
  color: #fff;
}

.font-bold {
  font-weight: 700;
}

.mb-8 {
  margin-bottom: 2rem;
}

.mt-16 {
  margin-top: 4rem;
}

.py-8 {
  padding-top: 2rem;
  padding-bottom: 2rem;
}

.py-4 {
  padding-top: 1rem;
  padding-bottom: 1rem;
}

.rounded {
  border-radius: 0.375rem;
}

.shadow-md {
  box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1),
    0 2px 4px -1px rgba(0, 0, 0, 0.06);
}

.overflow-hidden {
  overflow: hidden;
}

.w-full {
  width: 100%;
}

.h-48 {
  height: 12rem;
}

.object-cover {
  object-fit: cover;
}

.text-xl {
  font-size: 1.875rem;
}

.text-base {
  font-size: 1.125rem;
}

.inline-block {
  display: inline-block;
}

.py-2 {
  padding-top: 0.5rem;
  padding-bottom: 0.5rem;
}

.px-4 {
  padding-left: 1rem;
  padding-right: 1rem;
}</style>
