<template>
  <div class="min-h-screen bg-[#F3F5F6] font-sans flex flex-col">
    <header
      class="bg-white h-16 lg:h-20 flex items-center justify-between px-6 lg:px-16 shadow-sm"
    >
      <div
        class="text-[#D97706] text-2xl lg:text-3xl italic font-serif tracking-tight"
      >
        Chuks Kitchen
      </div>

      <nav
        class="hidden lg:flex items-center space-x-12 text-gray-700 font-medium"
      >
        <a href="#" class="hover:text-orange-500 transition">Home</a>
        <a href="#" class="hover:text-orange-500 transition">Explore</a>
        <a href="#" class="hover:text-orange-500 transition">My Orders</a>
        <a href="#" class="hover:text-orange-500 transition">Account</a>
      </nav>

      <div class="flex items-center">
        <button
          class="hidden lg:block bg-[#FD7E14] text-white px-10 py-2.5 rounded-lg font-semibold hover:bg-orange-600 transition"
        >
          Login
        </button>

        <button class="lg:hidden p-2 hover:opacity-70 transition">
          <svg
            class="w-6 h-6 text-gray-900"
            fill="none"
            stroke="currentColor"
            viewBox="0 0 24 24"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M4 6h16M4 12h16m-7 6h7"
            />
          </svg>
        </button>
      </div>
    </header>

    <main class="flex-grow flex items-start justify-center py-10 lg:py-20 px-4">
      <div
        class="bg-white rounded-xl shadow-sm p-8 lg:p-12 w-full max-w-[750px]"
      >
        <h2 class="text-2xl lg:text-3xl font-bold text-gray-900 mb-8">
          Delivery Details
        </h2>

        <div class="space-y-8">
          <div
            class="border border-gray-200 rounded-xl p-5 flex justify-between items-start group hover:border-orange-200 transition"
          >
            <div class="text-gray-700">
              <p class="font-medium">
                Home: 123 Main Street, Victoria Island, Lagos
              </p>
              <p class="text-sm text-gray-500 mt-1">
                Apt 4B, Opposite Mega Plaza
              </p>
            </div>
            <button class="text-blue-500 text-sm font-semibold hover:underline">
              Change Address
            </button>
          </div>

          <div class="space-y-3">
            <label class="block text-lg font-bold text-gray-900"
              >Delivery Time</label
            >
            <input
              type="text"
              value="ASAP(30-25)"
              class="w-full border border-gray-200 rounded-xl px-4 py-4 text-gray-700 focus:outline-none focus:ring-2 focus:ring-orange-500/20 focus:border-orange-500"
              readonly
            />
          </div>

          <div class="space-y-3">
            <label class="block text-lg font-bold text-gray-900"
              >Delivery Instructions (Optional)</label
            >
            <textarea
              v-model="instructions"
              placeholder="E.g leave at the front of the door, knock twice..."
              class="w-full border border-gray-200 rounded-xl px-4 py-4 text-gray-700 focus:outline-none focus:ring-2 focus:ring-orange-500/20 focus:border-orange-500 resize-none"
              rows="3"
            />
          </div>

          <div class="space-y-3">
            <label class="block text-lg font-bold text-gray-900"
              >Contact Address</label
            >
            <input
              type="tel"
              v-model="contactPhone"
              class="w-full border border-gray-200 rounded-xl px-4 py-4 text-gray-700 focus:outline-none focus:ring-2 focus:ring-orange-500/20 focus:border-orange-500"
            />
          </div>
        </div>
      </div>
    </main>

    <footer
      class="hidden lg:block bg-[#4B3621] text-white py-16 px-24 relative"
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
        <svg
          class="w-6 h-6 text-white"
          fill="none"
          stroke="currentColor"
          viewBox="0 0 24 24"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M5 10l7-7m0 0l7 7m-7-7v18"
          />
        </svg>
      </button>
    </footer>
  </div>
</template>

<script setup>
import { ref } from "vue";

const instructions = ref("");
const contactPhone = ref("+234 801 234 5678");

const scrollToTop = () => {
  window.scrollTo({ top: 0, behavior: "smooth" });
};
</script>

<style scoped>
/* Matching the elegant serif look from your logo */
.font-serif {
  font-family: "Times New Roman", Times, serif;
}
</style>
