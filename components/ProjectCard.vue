<template>
  <div class="bg-white rounded shadow-md overflow-hidden mb-4">
    <img class="w-full h-48 object-cover" :src="project.image" :alt="project.name" />
    <div class="px-6 py-4">
      <div class="font-bold text-xl mb-2">{{ project.name }}</div>
      <p class="text-gray-700 text-base">{{ project.description }}</p>
    </div>
    <div class="px-6 py-4">
      <router-link :to="{ name: 'ViewProject', params: { id: project.id } }"
        class="inline-block bg-indigo-600 hover:bg-indigo-700 text-white font-bold py-2 px-4 rounded">
        View project
      </router-link>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    project: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style lang="css">
.bg-white:hover img {
  position: relative;
}

.bg-white:hover img:before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border: 2px solid #4f46e5;
  border-radius: 0.375rem;
  transform: scale(0.9);
  opacity: 0;
  transition: all 0.2s ease-in-out;
}

.bg-white:hover img:before {
  transform: scale(1);
  opacity: 1;
}
</style>
