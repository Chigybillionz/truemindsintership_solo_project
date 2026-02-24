<template>
  <div class="w-full min-h-screen bg-[#F3F5F6] flex flex-col font-sans">
    <header
      class="bg-white h-20 flex items-center justify-between px-6 lg:px-20 shadow-sm border-b border-gray-100 sticky top-0 z-30"
    >
      <div class="flex items-center h-full">
        <img
          src="/logo.png"
          alt="Chuks Kitchen"
          class="h-8 lg:h-10 object-contain"
        />
      </div>

      <nav
        class="hidden lg:flex items-center h-full space-x-16 text-[#1A1A1A] font-medium"
      >
        <a href="#" class="cursor-wait hover:text-orange-500 transition-colors"
          >Home</a
        >
        <a href="#" class="cursor-wait hover:text-orange-500 transition-colors"
          >Explore</a
        >
        <a href="#" class="cursor-wait hover:text-orange-500 transition-colors"
          >My Orders</a
        >
        <a href="#" class="cursor-wait hover:text-orange-500 transition-colors"
          >Account</a
        >
      </nav>

      <div class="flex items-center h-full">
        <button
          class="hidden lg:block bg-[#FD7E14] opacity-80 cursor-wait text-white px-10 py-2.5 rounded-lg font-bold transition-all"
        >
          Login
        </button>

        <button class="lg:hidden flex items-center p-1">
          <img src="/menu.png" alt="Menu" class="w-7 h-7" />
        </button>
      </div>
    </header>

    <div class="flex-grow flex items-center justify-center">
      <div class="w-20 h-20 lg:w-24 lg:h-24">
        <img
          src="/loading.png"
          alt="Loading..."
          class="animate-spin w-full h-full object-contain"
        />
      </div>
    </div>

    <footer
      class="hidden lg:block bg-[#4B3621] text-white py-16 px-6 lg:px-24 relative"
    >
      <div
        class="max-w-7xl mx-auto grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-12"
      >
        <div>
          <h3 class="text-orange-400 text-3xl mb-4 italic font-serif">
            Chuks Kitchen
          </h3>
          <p class="text-gray-300 leading-relaxed">
            Bringing the authentic flavors of Nigerian home cooking to your
            table.
          </p>
          <p class="text-xs text-gray-400 mt-8">
            © 2026 Lift Media. All rights reserved.
          </p>
        </div>

        <div>
          <h4 class="font-bold text-lg mb-6">Quick Links</h4>
          <ul class="space-y-3 text-gray-300 text-sm">
            <li>
              <a href="#" class="hover:text-orange-400 transition">Home</a>
            </li>
            <li>
              <a href="#" class="hover:text-orange-400 transition">Explore</a>
            </li>
            <li>
              <a href="#" class="hover:text-orange-400 transition">My Order</a>
            </li>
            <li>
              <a href="#" class="hover:text-orange-400 transition">Account</a>
            </li>
            <li>
              <a href="#" class="hover:text-orange-400 transition">Contact</a>
            </li>
          </ul>
        </div>

        <div>
          <h4 class="font-bold text-lg mb-6">Contact Us</h4>
          <p class="text-gray-300 text-sm leading-7">
            +234 801 234 5678<br />hello@chukskitchen.com<br />123 Taste Blvd,
            Lagos, Nigeria
          </p>
        </div>

        <div>
          <h4 class="font-bold text-lg mb-4">Socials</h4>
          <ul class="space-y-3 text-gray-300 text-sm">
            <li>
              <a href="#" class="hover:text-orange-400 transition">Facebook</a>
            </li>
            <li>
              <a href="#" class="hover:text-orange-400 transition">Twitter</a>
            </li>
            <li>
              <a href="#" class="hover:text-orange-400 transition">LinkedIn</a>
            </li>
            <li>
              <a href="#" class="hover:text-orange-400 transition">Instagram</a>
            </li>
          </ul>
        </div>
      </div>

      <button
        @click="scrollToTop"
        class="absolute bottom-8 right-8 bg-blue-500 p-3 rounded-full hover:bg-blue-600 transition shadow-lg"
      >
        <img src="/arrowup.png" alt="Up" class="w-6 h-6" />
      </button>
    </footer>
  </div>
</template>

<script setup>
const scrollToTop = () => {
  window.scrollTo({ top: 0, behavior: "smooth" });
};
</script>

<style scoped>
.cursor-wait {
  cursor: wait;
}
.font-serif {
  font-family: Georgia, "Times New Roman", Times, serif;
}
</style>
