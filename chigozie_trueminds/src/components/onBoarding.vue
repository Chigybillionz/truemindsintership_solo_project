<template>
  <div class="min-h-screen w-full bg-white font-sans">
    <div class="lg:hidden">
      <div class="mx-4 mt-4 h-48 overflow-hidden rounded-2xl">
        <img
          src="/desktoponboarding.png"
          alt="Nigerian Food"
          class="w-full h-full object-cover"
        />
      </div>

      <div class="flex justify-end px-4 py-3">
        <button
          class="border-2 border-blue-500 text-blue-500 bg-white px-6 py-2 rounded-2xl font-semibold text-sm"
        >
          Sign In
        </button>
      </div>

      <div class="px-6 pb-8">
        <h2 class="text-center text-orange-400 font-script text-3xl mb-5">
          Chuks Kitchen
        </h2>
        <h1 class="font-bold text-[32px] leading-[40px] text-[#1F2937] mb-4">
          Your Authentic Taste of Nigeria
        </h1>
        <p class="text-gray-500 mb-8 leading-relaxed text-sm">
          Experience homemade flavors delivered fresh to your desk or home. We
          bring the rich culinary heritage of Nigeria right to your doorstep.
        </p>

        <div class="space-y-3 mb-10">
          <div
            v-for="feature in features"
            :key="feature.label"
            class="flex items-center gap-4 bg-gray-100 rounded-2xl p-4"
          >
            <div
              class="bg-orange-100 p-2 rounded-xl flex items-center justify-center"
            >
              <img :src="feature.icon" :alt="feature.label" class="w-6 h-6" />
            </div>
            <p class="font-semibold text-gray-700">{{ feature.label }}</p>
          </div>
        </div>

        <button
          class="w-full bg-orange-500 text-white py-4 rounded-2xl font-semibold text-lg mb-4"
        >
          Start Your Order
        </button>
        <button
          class="w-full border-2 border-blue-500 text-blue-500 py-4 rounded-2xl font-semibold text-lg"
        >
          Learn More About Us
        </button>
      </div>
    </div>

    <section class="hidden lg:flex min-h-screen flex-row">
      <div class="w-1/2 overflow-hidden">
        <img
          src="/desktoponboarding.png"
          alt="Family eating"
          class="w-full h-full object-cover"
        />
      </div>

      <div class="w-1/2 flex flex-col px-16 py-12 relative">
        <header class="flex justify-between items-center mb-24">
          <img src="/logo.png" alt="Logo" class="h-12 object-contain" />
          <button
            class="border border-blue-400 text-blue-500 px-8 py-2 rounded-xl font-medium"
          >
            Sign In
          </button>
        </header>

        <div class="max-w-xl">
          <h1 class="text-5xl font-bold text-gray-800 mb-6 leading-tight">
            Your Authentic Taste of Nigeria
          </h1>
          <p class="text-gray-600 text-lg mb-10 leading-relaxed">
            Experience homemade flavors delivered fresh to your desk or home. We
            bring the rich culinary heritage of Nigeria right to your doorstep.
          </p>

          <div class="grid grid-cols-2 gap-6 mb-12">
            <div
              v-for="feature in features"
              :key="feature.label"
              class="flex items-center gap-4"
            >
              <div class="bg-orange-100 p-2 rounded-lg">
                <img :src="feature.icon" :alt="feature.label" class="w-8 h-8" />
              </div>
              <span class="font-semibold text-gray-700 text-sm">{{
                feature.label
              }}</span>
            </div>
          </div>

          <div class="flex flex-col gap-4">
            <button
              class="w-full bg-orange-500 text-white py-4 rounded-xl font-bold text-lg hover:shadow-lg"
            >
              Start Your Order
            </button>
            <button
              class="w-full border-2 border-blue-400 text-blue-500 py-4 rounded-xl font-bold text-lg"
            >
              Learn More About Us
            </button>
          </div>
        </div>

        <footer
          class="mt-auto pt-12 flex justify-end gap-6 text-sm text-gray-400"
        >
          <span>© 2024 Chuks Kitchen.</span>
          <a href="#" class="hover:underline">Privacy Policy</a>
          <a href="#" class="hover:underline">Terms of Service</a>
        </footer>
      </div>
    </section>

    <footer
      class="hidden lg:block bg-[#4B3621] text-white py-16 px-6 lg:px-24 relative"
    >
      <div
        class="max-w-7xl mx-auto grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-12"
      >
        <div>
          <h3 class="font-script text-orange-400 text-3xl mb-4 italic">
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
            <li><a href="#" class="hover:text-orange-400">Home</a></li>
            <li><a href="#" class="hover:text-orange-400">Explore</a></li>
            <li><a href="#" class="hover:text-orange-400">My Order</a></li>
            <li><a href="#" class="hover:text-orange-400">Account</a></li>
            <li><a href="#" class="hover:text-orange-400">Contact</a></li>
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
            <li><a href="#" class="hover:text-orange-400">Facebook</a></li>
            <li><a href="#" class="hover:text-orange-400">Twitter</a></li>
            <li><a href="#" class="hover:text-orange-400">LinkedIn</a></li>
            <li><a href="#" class="hover:text-orange-400">Instagram</a></li>
          </ul>
        </div>
      </div>
      <button
        @click="scrollToTop"
        class="absolute bottom-8 right-8 bg-blue-500 p-3 rounded-full hover:bg-blue-600"
      >
        <img src="/arrowup.png" alt="Up" class="w-6 h-6" />
      </button>
    </footer>
  </div>
</template>

<script setup>
const features = [
  { label: "Freshly Prepared", icon: "/support.png" },
  { label: "Support Local Business", icon: "/support.png" },
  { label: "Fast & Reliable Delivery", icon: "/fastdelivery.png" },
];

const scrollToTop = () => {
  window.scrollTo({ top: 0, behavior: "smooth" });
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Great+Vibes&display=swap");
.font-script {
  font-family: "Great Vibes", cursive;
}
</style>
