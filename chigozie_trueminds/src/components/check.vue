<template>
  <div class="min-h-screen bg-white font-sans">
    <div
      class="min-h-screen bg-gray-50 flex items-center justify-center px-4 py-8"
    >
      <div class="w-full max-w-md">
        <!-- Logo -->
        <div class="text-center mb-8">
          <h1 class="text-3xl font-serif text-orange-500 mb-2">
            Chuko Kitchen
          </h1>
          <h2 class="text-2xl font-bold text-gray-900">Create Your Account</h2>
        </div>

        <form @submit.prevent="handleSignup" class="space-y-5">
          <!-- Email Input -->
          <div>
            <label class="block text-sm font-medium text-gray-700 mb-2">
              Email or username
            </label>
            <div class="relative">
              <svg
                class="absolute left-3 top-3 w-5 h-5 text-gray-400"
                viewBox="0 0 17 14"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M1.66667 13.3333C1.20833 13.3333 0.816111 13.1703 0.49 12.8442C0.163333 12.5175 0 12.125 0 11.6667V1.66667C0 1.20833 0.163333 0.816111 0.49 0.49C0.816111 0.163333 1.20833 0 1.66667 0H15C15.4583 0 15.8508 0.163333 16.1775 0.49C16.5036 0.816111 16.6667 1.20833 16.6667 1.66667V11.6667C16.6667 12.125 16.5036 12.5175 16.1775 12.8442C15.8508 13.1703 15.4583 13.3333 15 13.3333H1.66667ZM8.33333 7.35417C8.40278 7.35417 8.47556 7.34361 8.55167 7.3225C8.62833 7.30194 8.70139 7.27083 8.77083 7.22917L14.6667 3.54167C14.7778 3.47222 14.8611 3.38556 14.9167 3.28167C14.9722 3.17722 15 3.0625 15 2.9375C15 2.65972 14.8819 2.45139 14.6458 2.3125C14.4097 2.17361 14.1667 2.18056 13.9167 2.33333L8.33333 5.83333L2.75 2.33333C2.5 2.18056 2.25694 2.17694 2.02083 2.3225C1.78472 2.46861 1.66667 2.67361 1.66667 2.9375C1.66667 3.07639 1.69444 3.19778 1.75 3.30167C1.80556 3.40611 1.88889 3.48611 2 3.54167L7.89583 7.22917C7.96528 7.27083 8.03833 7.30194 8.115 7.3225C8.19111 7.34361 8.26389 7.35417 8.33333 7.35417Z"
                  fill="currentColor"
                />
              </svg>
              <input
                v-model="form.email"
                type="email"
                placeholder="name@gmail.com"
                class="w-full pl-10 pr-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-orange-500 focus:border-transparent"
                required
              />
            </div>
          </div>

          <!-- Phone Number Input -->
          <div>
            <label class="block text-sm font-medium text-gray-700 mb-2">
              Phone number
            </label>
            <div class="relative">
              <svg
                class="absolute left-3 top-3 w-5 h-5 text-gray-400"
                viewBox="0 0 15 15"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                text-gray-400 width="15" height="15" viewBox="0 0 15 15"
                fill="none" xmlns="http://www.w3.org/2000/svg" >
                <path
                  d="M14.125 15C12.3333 15 10.5869 14.6006 8.88583 13.8017C7.18417 13.0033 5.67722 11.9478 4.365 10.635C3.05222 9.32278 1.99667 7.81583 1.19833 6.11417C0.399445 4.41306 0 2.66667 0 0.875C0 0.625 0.0833333 0.416667 0.25 0.25C0.416667 0.0833333 0.625 0 0.875 0H4.25C4.44444 0 4.61806 0.0624999 4.77083 0.1875C4.92361 0.3125 5.01389 0.472222 5.04167 0.666667L5.58333 3.58333C5.61111 3.77778 5.60778 3.95472 5.57333 4.11417C5.53833 4.27417 5.45833 4.41667 5.33333 4.54167L3.33333 6.58333C3.91667 7.58333 4.64583 8.52083 5.52083 9.39583C6.39583 10.2708 7.36111 11.0278 8.41667 11.6667L10.375 9.70833C10.5 9.58333 10.6633 9.48944 10.865 9.42667C11.0661 9.36444 11.2639 9.34722 11.4583 9.375L14.3333 9.95833C14.5278 10 14.6875 10.0936 14.8125 10.2392C14.9375 10.3853 15 10.5556 15 10.75V14.125C15 14.375 14.9167 14.5833 14.75 14.75C14.5833 14.9167 14.375 15 14.125 15Z"
                  fill="#616161"
                />
              </svg>

              <input
                v-model="form.phone"
                type="tel"
                placeholder="8123340690"
                class="w-full pl-10 pr-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-orange-500 focus:border-transparent"
                required
              />
            </div>
          </div>

          <!-- Password Input -->

          <!-- Password Input -->
          <div>
            <label class="block text-sm font-medium text-gray-700 mb-2">
              password
            </label>
            <div class="relative">
              <svg
                class="absolute left-3 top-3 w-5 h-5 text-gray-400"
                viewBox="0 0 20 20"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M5.00004 18.333C4.54171 18.333 4.14948 18.17 3.82337 17.8438C3.49671 17.5172 3.33337 17.1247 3.33337 16.6663V8.33301C3.33337 7.87467 3.49671 7.48217 3.82337 7.15551C4.14948 6.8294 4.54171 6.66634 5.00004 6.66634H5.83337V4.99967C5.83337 3.8469 6.23976 2.86412 7.05254 2.05134C7.86476 1.23912 8.84726 0.833008 10 0.833008C11.1528 0.833008 12.1356 1.23912 12.9484 2.05134C13.7606 2.86412 14.1667 3.8469 14.1667 4.99967V6.66634H15C15.4584 6.66634 15.8509 6.8294 16.1775 7.15551C16.5037 7.48217 16.6667 7.87467 16.6667 8.33301V16.6663C16.6667 17.1247 16.5037 17.5172 16.1775 17.8438C15.8509 18.17 15.4584 18.333 15 18.333H5.00004ZM10 14.1663C10.4584 14.1663 10.8509 14.0033 11.1775 13.6772C11.5037 13.3505 11.6667 12.958 11.6667 12.4997C11.6667 12.0413 11.5037 11.6488 11.1775 11.3222C10.8509 10.9961 10.4584 10.833 10 10.833C9.54171 10.833 9.14949 10.9961 8.82337 11.3222C8.49671 11.6488 8.33337 12.0413 8.33337 12.4997C8.33337 12.958 8.49671 13.3505 8.82337 13.6772C9.14949 14.0033 9.54171 14.1663 10 14.1663ZM7.50004 6.66634H12.5V4.99967C12.5 4.30523 12.257 3.71495 11.7709 3.22884C11.2848 2.74273 10.6945 2.49967 10 2.49967C9.3056 2.49967 8.71532 2.74273 8.22921 3.22884C7.7431 3.71495 7.50004 4.30523 7.50004 4.99967V6.66634Z"
                  fill="currentColor"
                />
              </svg>

              <input
                v-model="form.confirmPassword"
                type="password"
                placeholder="QWE123#"
                class="w-full pl-10 pr-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-orange-500 focus:border-transparent"
                required
              />
            </div>
          </div>
          <div>
            <label class="block text-sm font-medium text-gray-700 mb-2">
              Confirm password
            </label>
            <div class="relative">
              <svg
                class="absolute left-3 top-3 w-5 h-5 text-gray-400"
                viewBox="0 0 20 20"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M5.00004 18.333C4.54171 18.333 4.14948 18.17 3.82337 17.8438C3.49671 17.5172 3.33337 17.1247 3.33337 16.6663V8.33301C3.33337 7.87467 3.49671 7.48217 3.82337 7.15551C4.14948 6.8294 4.54171 6.66634 5.00004 6.66634H5.83337V4.99967C5.83337 3.8469 6.23976 2.86412 7.05254 2.05134C7.86476 1.23912 8.84726 0.833008 10 0.833008C11.1528 0.833008 12.1356 1.23912 12.9484 2.05134C13.7606 2.86412 14.1667 3.8469 14.1667 4.99967V6.66634H15C15.4584 6.66634 15.8509 6.8294 16.1775 7.15551C16.5037 7.48217 16.6667 7.87467 16.6667 8.33301V16.6663C16.6667 17.1247 16.5037 17.5172 16.1775 17.8438C15.8509 18.17 15.4584 18.333 15 18.333H5.00004ZM10 14.1663C10.4584 14.1663 10.8509 14.0033 11.1775 13.6772C11.5037 13.3505 11.6667 12.958 11.6667 12.4997C11.6667 12.0413 11.5037 11.6488 11.1775 11.3222C10.8509 10.9961 10.4584 10.833 10 10.833C9.54171 10.833 9.14949 10.9961 8.82337 11.3222C8.49671 11.6488 8.33337 12.0413 8.33337 12.4997C8.33337 12.958 8.49671 13.3505 8.82337 13.6772C9.14949 14.0033 9.54171 14.1663 10 14.1663ZM7.50004 6.66634H12.5V4.99967C12.5 4.30523 12.257 3.71495 11.7709 3.22884C11.2848 2.74273 10.6945 2.49967 10 2.49967C9.3056 2.49967 8.71532 2.74273 8.22921 3.22884C7.7431 3.71495 7.50004 4.30523 7.50004 4.99967V6.66634Z"
                  fill="currentColor"
                />
              </svg>
              <input
                v-model="form.confirmPassword"
                type="password"
                placeholder="QWE123#"
                class="w-full pl-10 pr-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-orange-500 focus:border-transparent"
                required
              />
            </div>
          </div>

          <!-- Terms & Conditions Checkbox -->
          <div class="flex items-start space-x-3">
            <input
              v-model="form.acceptTerms"
              type="checkbox"
              id="terms"
              class="mt-1 w-4 h-4 text-blue-500 bg-white border-blue-300 rounded focus:ring-2 focus:ring-blue-500 cursor-pointer"
              required
            />
            <label for="terms" class="text-sm text-gray-700 cursor-pointer">
              I agree to the
              <a href="#" class="text-blue-400 hover:text-blue-600 font-medium"
                >Terms & Conditions</a
              >
              and
              <a href="#" class="text-blue-500 hover:text-blue-600 font-medium"
                >Privacy Policy</a
              >
            </label>
          </div>

          <!-- Continue Button -->
          <button
            type="submit"
            class="w-full bg-orange-500 hover:bg-orange-600 text-white font-semibold py-3 rounded-lg transition duration-200"
          >
            Continue
          </button>
        </form>

        <!-- Divider -->
        <div class="flex items-center my-6">
          <div class="flex-1 border-t border-gray-300"></div>
          <span class="px-3 text-sm text-gray-500">Or continue with</span>
          <div class="flex-1 border-t border-gray-300"></div>
        </div>

        <!-- Social Login Buttons -->
        <div class="space-y-3">
          <button
            type="button"
            @click="handleGoogleSignup"
            class="w-full flex items-center justify-center space-x-2 px-4 py-3 border border-gray-300 rounded-lg hover:bg-gray-50 transition duration-200"
          >
            <svg
              class="w-5 h-5"
              viewBox="0 0 24 24"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M22.56 12.25c0-.78-.07-1.53-.2-2.25H12v4.26h5.92c-.26 1.37-1.04 2.53-2.21 3.31v2.77h3.57c2.08-1.92 3.28-4.74 3.28-8.09z"
                fill="#4285F4"
              />
              <path
                d="M12 23c2.97 0 5.46-.98 7.28-2.66l-3.57-2.77c-.98.66-2.23 1.06-3.71 1.06-2.86 0-5.29-1.93-6.16-4.53H2.18v2.84C3.99 20.53 7.7 23 12 23z"
                fill="#34A853"
              />
              <path
                d="M5.84 14.09c-.22-.66-.35-1.36-.35-2.09s.13-1.43.35-2.09V7.07H2.18C1.43 8.55 1 10.22 1 12s.43 3.45 1.18 4.93l2.85-2.22.81-.62z"
                fill="#FBBC05"
              />
              <path
                d="M12 5.38c1.62 0 3.06.56 4.21 1.64l3.15-3.15C17.45 2.09 14.97 1 12 1 7.7 1 3.99 3.47 2.18 7.07l3.66 2.84c.87-2.6 3.3-4.53 6.16-4.53z"
                fill="#EA4335"
              />
            </svg>
            <span class="text-gray-700 font-medium">Continue with Google</span>
          </button>

          <button
            type="button"
            @click="handleAppleSignup"
            class="w-full flex items-center justify-center space-x-2 px-4 py-3 border border-gray-300 rounded-lg hover:bg-gray-50 transition duration-200"
          >
            <svg
              width="40"
              height="40"
              viewBox="0 0 40 40"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M24.6796 21.2493L25.2495 17.6314H21.7388V15.2798C21.7388 14.2906 22.2289 13.3239 23.7962 13.3239H25.4148V10.2431C24.4722 10.0929 23.5198 10.0117 22.5652 10C19.6757 10 17.7893 11.7354 17.7893 14.8728V17.6314H14.5863V21.2493H17.7893V30H21.7388V21.2493H24.6796Z"
                fill="#337FFF"
              />
            </svg>

            <span class="text-gray-700 font-medium">Continue with Apple</span>
          </button>
        </div>

        <!-- Sign In Link -->
        <p class="text-center mt-6 text-gray-700 text-sm">
          Already have an account?
          <a href="#" class="text-blue-500 hover:text-blue-600 font-medium"
            >Sign in</a
          >
        </p>
      </div>
    </div>

    <div class="hidden md:flex min-h-screen">
      <div class="w-1/2 relative">
        <img
          src="/desktoponboarding.png"
          class="absolute inset-0 w-full h-full object-cover"
        />
        <div class="absolute inset-0 bg-orange-900/40"></div>
        <div
          class="absolute inset-0 flex items-center justify-center p-12 text-center text-white"
        >
          <div>
            <h1 class="text-5xl font-bold mb-6">Chuks Kitchen</h1>
            <p class="text-xl max-w-md mx-auto leading-relaxed">
              Your journey to delicious, authentic Nigerian meals starts here.
              Join us today!
            </p>
          </div>
        </div>
      </div>

      <div class="w-1/2 bg-white p-12 overflow-y-auto">
        <div class="text-center mb-10">
          <img src="/logo.png" alt="Logo" class="h-10 mx-auto" />
          <h2 class="text-3xl font-bold text-gray-800 mt-6">
            Create Your Account
          </h2>
        </div>

        <form @submit.prevent="handleSignup" class="max-w-md mx-auto space-y-5">
          <div>
            <label class="block text-sm font-medium text-gray-700 mb-1"
              >Email address</label
            >
            <input
              v-model="form.email"
              type="email"
              placeholder="name@gmail.com"
              class="input-field-desktop"
              required
            />
          </div>

          <div>
            <label class="block text-sm font-medium text-gray-700 mb-1"
              >Phone number</label
            >
            <input
              v-model="form.phone"
              type="tel"
              placeholder="0812 345 6789"
              class="input-field-desktop"
              required
            />
          </div>

          <div class="grid grid-cols-2 gap-4">
            <div>
              <label class="block text-sm font-medium text-gray-700 mb-1"
                >Password</label
              >
              <input
                v-model="form.password"
                type="password"
                placeholder="••••••••"
                class="input-field-desktop"
                required
              />
            </div>
            <div>
              <label class="block text-sm font-medium text-gray-700 mb-1"
                >Confirm</label
              >
              <input
                v-model="form.confirmPassword"
                type="password"
                placeholder="••••••••"
                class="input-field-desktop"
                required
              />
            </div>
          </div>

          <div class="flex items-center gap-2">
            <input
              v-model="form.acceptTerms"
              type="checkbox"
              id="terms-dt"
              class="rounded text-orange-500 focus:ring-orange-500"
              required
            />
            <label for="terms-dt" class="text-sm text-gray-600">
              I agree to the
              <a href="#" class="text-blue-500">Terms & Conditions</a>
            </label>
          </div>

          <button
            type="submit"
            class="w-full bg-orange-500 hover:bg-orange-600 text-white font-bold py-4 rounded-xl shadow-lg transition duration-200"
          >
            Create Account
          </button>

          <div class="relative my-6">
            <div class="absolute inset-0 flex items-center">
              <div class="w-full border-t border-gray-100"></div>
            </div>
            <div class="relative flex justify-center text-xs uppercase">
              <span class="bg-white px-2 text-gray-400">Or continue with</span>
            </div>
          </div>

          <div class="flex gap-4">
            <button type="button" class="social-btn-desktop">
              <img src="/google.png" class="w-5 h-5" /> Google
            </button>
            <button type="button" class="social-btn-desktop">
              <img src="/facebook.png" class="w-5 h-5" /> Apple
            </button>
          </div>

          <p class="text-center text-sm text-gray-600 pt-4">
            Already have an account?
            <a href="#" class="text-blue-500 font-bold">Sign in</a>
          </p>
        </form>
      </div>
    </div>

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
import { reactive, ref } from "vue";

const form = reactive({
  email: "",
  phone: "",
  password: "",
  confirmPassword: "",
  acceptTerms: false,
});

const showPassword = ref(false);

const handleSignup = () => {
  if (form.password !== form.confirmPassword) {
    alert("Passwords do not match!");
    return;
  }
  console.log("Signup form submitted:", form);
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Great+Vibes&display=swap");

.font-script {
  font-family: "Great Vibes", cursive;
}

.input-field {
  @apply w-full pl-10 pr-4 py-3 border border-gray-200 rounded-xl focus:outline-none focus:ring-2 focus:ring-orange-500 focus:border-transparent transition-all;
}

.input-field-desktop {
  @apply w-full px-4 py-3 border border-gray-100 bg-gray-50 rounded-xl focus:outline-none focus:ring-2 focus:ring-orange-500 transition-all;
}

.social-btn {
  @apply w-full flex items-center justify-center gap-3 py-3 border border-gray-200 rounded-xl hover:bg-gray-50 font-medium text-gray-700 transition-all;
}

.social-btn-desktop {
  @apply flex-1 flex items-center justify-center gap-2 py-3 border border-gray-200 rounded-xl hover:bg-gray-50 font-medium text-gray-700 transition-all;
}
</style>
