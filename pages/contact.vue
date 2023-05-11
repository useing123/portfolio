<template>
    <div class="flex flex-col min-h-screen">
      <Header />
      <div class="flex-grow">
    <div class="container mx-auto px-4 py-8">
    <h1 class="text-2xl font-bold mb-4">Contact Us</h1>
    <p class="mb-4">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam eget dui nulla. Etiam auctor faucibus mi, quis tempus dolor tincidunt vel. Ut feugiat urna eget risus pellentesque imperdiet. Donec a lacinia arcu. Pellentesque pharetra finibus nunc quis ullamcorper. Suspendisse potenti. Sed feugiat nisl sit amet ultrices tristique.</p>
    <p class="mb-4">Please feel free to contact us if you have any questions or comments. You can reach us at:</p>
    <ul class="list-disc ml-8 mb-4">
      <li>Email: info@myportfolio.com</li>
      <li>Phone: 555-1234</li>
      <li>Address: 123 Main St, Anytown, USA</li>
    </ul>
    <p class="mb-4">We look forward to hearing from you!</p>
    </div>
      </div>
      <Footer />
    </div>
  </template>
  
  <script>
  import Header from '~/components/Header.vue'
  import Footer from '~/components/Footer.vue'
  
  export default {
    components: {
      Header,
      Footer
    }
  }
  </script>
  