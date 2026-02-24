<template>
  <div class="min-h-screen bg-white">
    <!-- MOBILE VIEW -->
    <div class="md:hidden flex flex-col min-h-screen">
      <!-- Logo -->
      <div class="text-center pt-8 mb-6">
        <img src="/logo.png" alt="Chuks Kitchen" class="h-8 mx-auto" />
        <h2 class="text-2xl font-bold text-dark mt-4">Login your Account</h2>
      </div>

      <!-- Form Container -->
      <div class="px-6 flex-1">
        <!-- Email Input -->
        <div class="mb-6">
          <label class="block text-sm font-medium text-gray-700 mb-2">
            Email or phone number
          </label>
          <div class="relative">
            <div class="absolute left-3 top-3.5 text-gray-400">
              <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20">
                <path
                  d="M2.003 5.884L10 9.882l7.997-3.998A2 2 0 0016 4H4a2 2 0 00-1.997 1.884z"
                ></path>
                <path
                  d="M18 8.118l-8 4-8-4V14a2 2 0 002 2h12a2 2 0 002-2V8.118z"
                ></path>
              </svg>
            </div>
            <input
              v-model="email"
              type="email"
              placeholder="name@gmail.com"
              class="w-full pl-10 pr-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-secondary focus:border-transparent"
            />
          </div>
        </div>

        <!-- Password Input -->
        <div class="mb-2">
          <label class="block text-sm font-medium text-gray-700 mb-2">
            Password
          </label>
          <div class="relative">
            <div class="absolute left-3 top-3.5 text-gray-400">
              <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20">
                <path
                  fill-rule="evenodd"
                  d="M5 9V7a5 5 0 0110 0v2a2 2 0 012 2v5a2 2 0 01-2 2H5a2 2 0 01-2-2v-5a2 2 0 012-2zm8-2v2H7V7a3 3 0 016 0z"
                  clip-rule="evenodd"
                ></path>
              </svg>
            </div>
            <input
              v-model="password"
              :type="showPassword ? 'text' : 'password'"
              placeholder="••••••"
              class="w-full pl-10 pr-12 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-secondary focus:border-transparent"
            />
            <button
              type="button"
              @click="showPassword = !showPassword"
              class="absolute right-3 top-3.5 text-gray-400 hover:text-gray-600"
            >
              <svg
                v-if="!showPassword"
                class="w-5 h-5"
                fill="currentColor"
                viewBox="0 0 20 20"
              >
                <path d="M10 12a2 2 0 100-4 2 2 0 000 4z"></path>
                <path
                  fill-rule="evenodd"
                  d="M.458 10C1.732 5.943 5.522 3 10 3s8.268 2.943 9.542 7c-1.274 4.057-5.064 7-9.542 7S1.732 14.057.458 10zM14 10a4 4 0 11-8 0 4 4 0 018 0z"
                  clip-rule="evenodd"
                ></path>
              </svg>
              <svg
                v-else
                class="w-5 h-5"
                fill="currentColor"
                viewBox="0 0 20 20"
              >
                <path
                  fill-rule="evenodd"
                  d="M3.707 2.293a1 1 0 00-1.414 1.414l14 14a1 1 0 001.414-1.414l-1.473-1.473A10.014 10.014 0 0019.542 10C18.268 5.943 14.478 3 10 3a9.958 9.958 0 00-4.512 1.074l-1.78-1.781zm4.261 4.26l1.514 1.515a2.003 2.003 0 012.45 2.45l1.514 1.514a4 4 0 00-5.478-5.478z"
                  clip-rule="evenodd"
                ></path>
                <path
                  d="M15.171 11.586a4 4 0 111.414-1.414l1.473 1.473c.078.088.157.177.235.266A10.015 10.015 0 0119.542 10c-1.274-4.057-5.064-7-9.542-7a9.958 9.958 0 00-4.512 1.074l1.781 1.781a7.977 7.977 0 019.354 9.33z"
                ></path>
              </svg>
            </button>
          </div>
        </div>

        <!-- Forgot Password -->
        <div class="text-right mb-6">
          <a
            href="#"
            class="text-sm text-primary hover:text-secondary font-medium"
          >
            Forgot Password?
          </a>
        </div>

        <!-- Continue Button -->
        <button
          @click="handleLogin"
          class="w-full bg-secondary hover:bg-orange-600 text-white font-bold py-3 rounded-lg transition duration-200 mb-4"
        >
          Continue
        </button>

        <!-- Or continue with -->
        <div class="text-center mb-4">
          <p class="text-sm text-gray-600">Or continue with</p>
        </div>

        <!-- Social Login Buttons -->
        <div class="space-y-3 mb-6">
          <button
            class="w-full flex items-center justify-center gap-2 border border-gray-300 py-3 rounded-lg hover:bg-gray-50 transition duration-200"
          >
            <img src="/google.png" alt="Google" class="w-5 h-5" />
            Continue with Google
          </button>

          <button
            class="w-full flex items-center justify-center gap-2 border border-gray-300 py-3 rounded-lg hover:bg-gray-50 transition duration-200"
          >
            <img src="/facebook.png" alt="Facebook" class="w-5 h-5" />
            Continue with Apple
          </button>
        </div>

        <!-- Create Account -->
        <div class="text-center">
          <p class="text-sm text-gray-600">
            Don't have an account?
            <a href="#" class="text-primary hover:text-secondary font-medium">
              Create an account
            </a>
          </p>
        </div>
      </div>
    </div>

    <!-- DESKTOP VIEW -->
    <div class="hidden md:flex flex-col min-h-screen">
      <!-- Main Content -->
      <div class="flex flex-1">
        <!-- Left Side - Image with Overlay -->
        <div
          class="w-1/2 relative overflow-hidden"
          style="
            background-image: url('/desktoponboarding.png');
            background-size: cover;
            background-position: center;
          "
        >
          <!-- Orange Overlay -->
          <div class="absolute inset-0 bg-orange-800 opacity-40"></div>

          <!-- Content Overlay -->
          <div class="absolute inset-0 flex items-center justify-center">
            <div class="text-center text-white px-12">
              <h1 class="text-5xl font-bold mb-6">Chuks Kitchen</h1>
              <p class="text-xl leading-relaxed">
                Your journey to delicious, authentic Nigerian meals starts here.
                Sign up or log in to order your favorites today!
              </p>
            </div>
          </div>
        </div>

        <!-- Right Side - Login Form -->
        <div class="w-1/2 bg-white px-12 py-8 flex flex-col justify-between">
          <!-- Header -->
          <div class="mb-8">
            <img src="/logo.png" alt="Chuks Kitchen" class="h-8 mb-4" />
            <h2 class="text-3xl font-bold text-dark">Login your Account</h2>
          </div>

          <!-- Form Content -->
          <div class="flex-1 flex flex-col justify-center">
            <!-- Email Input -->
            <div class="mb-6">
              <label class="block text-sm font-medium text-gray-700 mb-2">
                Email or phone number
              </label>
              <div class="relative">
                <div class="absolute left-3 top-3.5 text-gray-400">
                  <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20">
                    <path
                      d="M2.003 5.884L10 9.882l7.997-3.998A2 2 0 0016 4H4a2 2 0 00-1.997 1.884z"
                    ></path>
                    <path
                      d="M18 8.118l-8 4-8-4V14a2 2 0 002 2h12a2 2 0 002-2V8.118z"
                    ></path>
                  </svg>
                </div>
                <input
                  v-model="email"
                  type="email"
                  placeholder="name@gmail.com"
                  class="w-full pl-10 pr-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-secondary focus:border-transparent"
                />
              </div>
            </div>

            <!-- Password Input -->
            <div class="mb-2">
              <label class="block text-sm font-medium text-gray-700 mb-2">
                Password
              </label>
              <div class="relative">
                <div class="absolute left-3 top-3.5 text-gray-400">
                  <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20">
                    <path
                      fill-rule="evenodd"
                      d="M5 9V7a5 5 0 0110 0v2a2 2 0 012 2v5a2 2 0 01-2 2H5a2 2 0 01-2-2v-5a2 2 0 012-2zm8-2v2H7V7a3 3 0 016 0z"
                      clip-rule="evenodd"
                    ></path>
                  </svg>
                </div>
                <input
                  v-model="password"
                  :type="showPassword ? 'text' : 'password'"
                  placeholder="••••••"
                  class="w-full pl-10 pr-12 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-secondary focus:border-transparent"
                />
                <button
                  type="button"
                  @click="showPassword = !showPassword"
                  class="absolute right-3 top-3.5 text-gray-400 hover:text-gray-600"
                >
                  <svg
                    v-if="!showPassword"
                    class="w-5 h-5"
                    fill="currentColor"
                    viewBox="0 0 20 20"
                  >
                    <path d="M10 12a2 2 0 100-4 2 2 0 000 4z"></path>
                    <path
                      fill-rule="evenodd"
                      d="M.458 10C1.732 5.943 5.522 3 10 3s8.268 2.943 9.542 7c-1.274 4.057-5.064 7-9.542 7S1.732 14.057.458 10zM14 10a4 4 0 11-8 0 4 4 0 018 0z"
                      clip-rule="evenodd"
                    ></path>
                  </svg>
                  <svg
                    v-else
                    class="w-5 h-5"
                    fill="currentColor"
                    viewBox="0 0 20 20"
                  >
                    <path
                      fill-rule="evenodd"
                      d="M3.707 2.293a1 1 0 00-1.414 1.414l14 14a1 1 0 001.414-1.414l-1.473-1.473A10.014 10.014 0 0019.542 10C18.268 5.943 14.478 3 10 3a9.958 9.958 0 00-4.512 1.074l-1.78-1.781zm4.261 4.26l1.514 1.515a2.003 2.003 0 012.45 2.45l1.514 1.514a4 4 0 00-5.478-5.478z"
                      clip-rule="evenodd"
                    ></path>
                    <path
                      d="M15.171 11.586a4 4 0 111.414-1.414l1.473 1.473c.078.088.157.177.235.266A10.015 10.015 0 0119.542 10c-1.274-4.057-5.064-7-9.542-7a9.958 9.958 0 00-4.512 1.074l1.781 1.781a7.977 7.977 0 019.354 9.33z"
                    ></path>
                  </svg>
                </button>
              </div>
            </div>

            <!-- Forgot Password -->
            <div class="text-right mb-8">
              <a
                href="#"
                class="text-sm text-blue-500 hover:text-secondary font-medium"
              >
                Forgot Password?
              </a>
            </div>

            <!-- Continue Button -->
            <button
              @click="handleLogin"
              class="w-full bg-secondary hover:bg-orange-600 text-white font-bold py-3 rounded-lg transition duration-200 mb-6"
            >
              Continue
            </button>

            <!-- Or continue with -->
            <div class="text-center mb-6">
              <p class="text-sm text-gray-600">Or continue with</p>
            </div>

            <!-- Social Login Buttons -->
            <div class="space-y-3 mb-6">
              <button
                class="w-full flex items-center justify-center gap-2 border border-gray-300 py-3 rounded-lg hover:bg-gray-50 transition duration-200"
              >
                <img src="/google.png" alt="Google" class="w-5 h-5" />
                Continue with Google
              </button>

              <button
                class="w-full flex items-center justify-center gap-2 border border-gray-300 py-3 rounded-lg hover:bg-gray-50 transition duration-200"
              >
                <img src="/facebook.png" alt="Facebook" class="w-5 h-5" />
                Continue with Apple
              </button>
            </div>

            <!-- Create Account -->
            <div class="text-center">
              <p class="text-sm text-gray-600">
                Don't have an account?
                <a
                  href="#"
                  class="text-primary hover:text-secondary font-medium"
                >
                  Create an account
                </a>
              </p>
            </div>
          </div>
        </div>
      </div>

      <!-- Footer -->
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
  </div>
</template>

<script setup>
import { ref } from "vue";

const email = ref("");
const password = ref("");
const showPassword = ref(false);

const handleLogin = () => {
  if (email.value && password.value) {
    console.log("Login:", { email: email.value, password: password.value });
  }
};
</script>

<style scoped>
button {
  transition: all 0.2s ease-in-out;
}

button:active {
  transform: scale(0.98);
}
</style>
