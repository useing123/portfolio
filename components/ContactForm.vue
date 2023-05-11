<template>
    <form class="flex flex-col space-y-6" @submit.prevent="submitForm">
      <div class="flex flex-col">
        <label class="text-sm font-medium text-gray-700 mb-1" for="name">Имя</label>
        <input
          class="w-full py-2 px-3 rounded-md border border-gray-400 text-gray-800 focus:outline-none focus:border-blue-500"
          type="text"
          id="name"
          v-model="name"
          required
        />
      </div>
      <div class="flex flex-col">
        <label class="text-sm font-medium text-gray-700 mb-1" for="email">Email</label>
        <input
          class="w-full py-2 px-3 rounded-md border border-gray-400 text-gray-800 focus:outline-none focus:border-blue-500"
          type="email"
          id="email"
          v-model="email"
          required
        />
      </div>
      <div class="flex flex-col">
        <label class="text-sm font-medium text-gray-700 mb-1" for="message">Сообщение</label>
        <textarea
          class="w-full py-2 px-3 rounded-md border border-gray-400 text-gray-800 focus:outline-none focus:border-blue-500"
          id="message"
          v-model="message"
          required
        ></textarea>
      </div>
      <div class="flex justify-left">
        <button
          class="py-2 px-6 bg-indigo-600 text-white font-semibold rounded-md shadow-md hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-offset-2"
          :disabled="isSubmitting"
          type="submit"
        >
          {{ isSubmitting ? 'Отправка...' : 'Отправить' }}
        </button>
      </div>
    </form>
  </template>
  
  <script>
  export default {
    data() {
      return {
        name: '',
        email: '',
        message: '',
        isSubmitting: false,
      };
    },
    methods: {
      async submitForm() {
        this.isSubmitting = true;
        // Здесь мы бы обычно отправили данные формы на сервер
        // и обработали бы ответ, но для примера оставим это пустым.
        await new Promise((resolve) => setTimeout(resolve, 2000));
        this.name = '';
        this.email = '';
        this.message = '';
        this.isSubmitting = false;
      },
    },
  };
  </script>
  