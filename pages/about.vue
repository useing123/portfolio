<template>
    <div class="flex flex-col min-h-screen">
      <Header />
    <div class="flex-grow">
        <div class="container mx-auto px-4 py-8">
        <h1 class="text-2xl font-bold mb-4">About Us</h1>
        <p class="mb-4">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam eget dui nulla. Etiam auctor faucibus mi, quis tempus dolor tincidunt vel. Ut feugiat urna eget risus pellentesque imperdiet. Donec a lacinia arcu. Pellentesque pharetra finibus nunc quis ullamcorper. Suspendisse potenti. Sed feugiat nisl sit amet ultrices tristique.</p>
        <p class="mb-4">In hac habitasse platea dictumst. Integer dapibus rhoncus purus, vel euismod mauris lacinia ac. In efficitur nulla vitae mi sagittis blandit. Proin ut sapien consectetur, tristique arcu eu, suscipit nunc. Praesent faucibus fermentum odio, sit amet bibendum lacus congue quis.</p>
        <p class="mb-4">Suspendisse in mauris et felis faucibus dignissim. Sed pretium, eros quis vulputate bibendum, eros nisl euismod sapien, eget posuere magna augue at nulla. Sed eget enim euismod, tristique massa a, pulvinar tellus. Integer volutpat eu nulla sed porttitor. Aliquam convallis, augue eget posuere gravida, augue odio convallis elit, in congue elit nisi ac nibh. Donec venenatis arcu et dolor lacinia, at posuere nibh iaculis. Nunc sed ultrices dolor. Fusce sollicitudin auctor felis a efficitur.</p>
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
  