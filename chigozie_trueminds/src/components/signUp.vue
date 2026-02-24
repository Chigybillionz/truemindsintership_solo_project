<template>
  <div class="min-h-screen bg-white">
    <!-- MOBILE VIEW -->
    <div class="md:hidden flex flex-col min-h-screen">
      <!-- Logo -->
      <div class="text-center pt-8 mb-6">
        <h1 class="text-2xl font-serif italic text-orange-500">
          Chuko Kitchen
        </h1>
        <h2 class="text-2xl font-bold text-dark mt-4">Create Your Account</h2>
      </div>

      <!-- Form Container -->
      <div class="px-6 flex-1 overflow-y-auto">
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
              class="w-full pl-10 pr-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-orange-500 focus:border-transparent"
            />
          </div>
        </div>

        <!-- Phone Number Input -->
        <div class="mb-6">
          <label class="block text-sm font-medium text-gray-700 mb-2">
            Phone number
          </label>
          <div class="relative">
            <div class="absolute left-3 top-3.5 text-gray-400">
              <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20">
                <path
                  d="M2 3a1 1 0 011-1h2.153a1 1 0 01.986.836l.74 4.435a1 1 0 01-.54 1.06l-1.81.905a16.113 16.113 0 006.416 6.416l.905-1.81a1 1 0 011.06-.54l4.435.74a1 1 0 01.836.986V17a1 1 0 01-1 1h-2C7.82 18 2 12.18 2 5V3z"
                ></path>
              </svg>
            </div>
            <input
              v-model="phone"
              type="tel"
              placeholder="+234 801 234 5678"
              class="w-full pl-10 pr-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-orange-500 focus:border-transparent"
            />
          </div>
        </div>

        <!-- Password Input -->
        <div class="mb-6">
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
              class="w-full pl-10 pr-12 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-orange-500 focus:border-transparent"
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

        <!-- Confirm Password Input -->
        <div class="mb-6">
          <label class="block text-sm font-medium text-gray-700 mb-2">
            Confirm password
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
              v-model="confirmPassword"
              type="password"
              placeholder="••••••"
              class="w-full pl-10 pr-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-orange-500 focus:border-transparent"
            />
          </div>
        </div>

        <!-- Terms & Conditions Checkbox -->
        <div class="flex items-start space-x-3 mb-6">
          <input
            v-model="acceptTerms"
            type="checkbox"
            id="terms"
            class="mt-1 w-4 h-4 text-orange-500 bg-white border-gray-300 rounded focus:ring-2 focus:ring-orange-500 cursor-pointer"
          />
          <label for="terms" class="text-sm text-gray-700 cursor-pointer">
            I agree to the
            <a href="#" class="text-blue-500 hover:text-blue-600 font-medium"
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
          @click="handleSignup"
          class="w-full bg-orange-500 hover:bg-orange-600 text-white font-bold py-3 rounded-lg transition duration-200 mb-4"
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
            </svg>
            Continue with Google
          </button>

          <button
            class="w-full flex items-center justify-center gap-2 border border-gray-300 py-3 rounded-lg hover:bg-gray-50 transition duration-200"
          >
            <svg
              class="w-5 h-5"
              fill="currentColor"
              viewBox="0 0 24 24"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M17.05 13.5c-.02-1.82.75-3.53 2.05-4.68-.95-1.32-2.42-2.12-4.06-2.12-1.73 0-3.24.99-3.96 2.46-.36.74-.61 1.54-.73 2.38-.13.85-.12 1.72.04 2.55.16.83.46 1.62.89 2.33.72 1.22 1.88 2.12 3.25 2.47 1.37.35 2.87.13 4.07-.59 1.2-.72 2.08-1.87 2.45-3.22.37-1.35.27-2.83-.25-4.15-.52-1.32-1.52-2.37-2.77-2.98-1.25-.61-2.71-.71-4.06-.28-1.35.43-2.54 1.28-3.35 2.42-.35.48-.63 1.01-.84 1.56-.21.55-.35 1.12-.41 1.7-.06.58-.04 1.16.08 1.72.12.56.34 1.09.66 1.57.32.48.74.91 1.24 1.26.5.35 1.07.63 1.67.82.6.19 1.23.29 1.86.28.63 0 1.25-.1 1.85-.29.6-.19 1.17-.47 1.67-.82.5-.35.92-.78 1.24-1.26.32-.48.54-1.01.66-1.57.12-.56.14-1.14.08-1.72"
              />
            </svg>
            Continue with Apple
          </button>
        </div>

        <!-- Create Account -->
        <div class="text-center mb-8">
          <p class="text-sm text-gray-600">
            Already have an account?
            <a href="#" class="text-blue-500 hover:text-blue-600 font-medium">
              Sign in
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
                Sign up today to order your favorites!
              </p>
            </div>
          </div>
        </div>

        <!-- Right Side - Signup Form -->
        <div
          class="w-1/2 bg-white px-12 py-8 flex flex-col justify-between overflow-y-auto"
        >
          <!-- Header -->
          <div class="mb-8">
            <h1 class="text-3xl font-serif italic text-orange-500 mb-2">
              Chuks Kitchen
            </h1>
            <h2 class="text-3xl font-bold text-dark">Create Your Account</h2>
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
                  class="w-full pl-10 pr-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-orange-500 focus:border-transparent"
                />
              </div>
            </div>

            <!-- Phone Number Input -->
            <div class="mb-6">
              <label class="block text-sm font-medium text-gray-700 mb-2">
                Phone number
              </label>
              <div class="relative">
                <div class="absolute left-3 top-3.5 text-gray-400">
                  <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20">
                    <path
                      d="M2 3a1 1 0 011-1h2.153a1 1 0 01.986.836l.74 4.435a1 1 0 01-.54 1.06l-1.81.905a16.113 16.113 0 006.416 6.416l.905-1.81a1 1 0 011.06-.54l4.435.74a1 1 0 01.836.986V17a1 1 0 01-1 1h-2C7.82 18 2 12.18 2 5V3z"
                    ></path>
                  </svg>
                </div>
                <input
                  v-model="phone"
                  type="tel"
                  placeholder="+234 801 234 5678"
                  class="w-full pl-10 pr-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-orange-500 focus:border-transparent"
                />
              </div>
            </div>

            <!-- Password Input -->
            <div class="mb-6">
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
                  class="w-full pl-10 pr-12 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-orange-500 focus:border-transparent"
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

            <!-- Confirm Password Input -->
            <div class="mb-6">
              <label class="block text-sm font-medium text-gray-700 mb-2">
                Confirm password
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
                  v-model="confirmPassword"
                  type="password"
                  placeholder="••••••"
                  class="w-full pl-10 pr-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-orange-500 focus:border-transparent"
                />
              </div>
            </div>

            <!-- Terms & Conditions Checkbox -->
            <div class="flex items-start space-x-3 mb-8">
              <input
                v-model="acceptTerms"
                type="checkbox"
                id="terms"
                class="mt-1 w-4 h-4 text-orange-500 bg-white border-gray-300 rounded focus:ring-2 focus:ring-orange-500 cursor-pointer"
              />
              <label for="terms" class="text-sm text-gray-700 cursor-pointer">
                I agree to the
                <a
                  href="#"
                  class="text-blue-500 hover:text-blue-600 font-medium"
                  >Terms & Conditions</a
                >
                and
                <a
                  href="#"
                  class="text-blue-500 hover:text-blue-600 font-medium"
                  >Privacy Policy</a
                >
              </label>
            </div>

            <!-- Continue Button -->
            <button
              @click="handleSignup"
              class="w-full bg-orange-500 hover:bg-orange-600 text-white font-bold py-3 rounded-lg transition duration-200 mb-6"
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
                </svg>
                Continue with Google
              </button>

              <button
                class="w-full flex items-center justify-center gap-2 border border-gray-300 py-3 rounded-lg hover:bg-gray-50 transition duration-200"
              >
                <svg
                  class="w-5 h-5"
                  fill="currentColor"
                  viewBox="0 0 24 24"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    d="M17.05 13.5c-.02-1.82.75-3.53 2.05-4.68-.95-1.32-2.42-2.12-4.06-2.12-1.73 0-3.24.99-3.96 2.46-.36.74-.61 1.54-.73 2.38-.13.85-.12 1.72.04 2.55.16.83.46 1.62.89 2.33.72 1.22 1.88 2.12 3.25 2.47 1.37.35 2.87.13 4.07-.59 1.2-.72 2.08-1.87 2.45-3.22.37-1.35.27-2.83-.25-4.15-.52-1.32-1.52-2.37-2.77-2.98-1.25-.61-2.71-.71-4.06-.28-1.35.43-2.54 1.28-3.35 2.42-.35.48-.63 1.01-.84 1.56-.21.55-.35 1.12-.41 1.7-.06.58-.04 1.16.08 1.72.12.56.34 1.09.66 1.57.32.48.74.91 1.24 1.26.5.35 1.07.63 1.67.82.6.19 1.23.29 1.86.28.63 0 1.25-.1 1.85-.29.6-.19 1.17-.47 1.67-.82.5-.35.92-.78 1.24-1.26.32-.48.54-1.01.66-1.57.12-.56.14-1.14.08-1.72"
                  />
                </svg>
                Continue with Apple
              </button>
            </div>

            <!-- Sign In Link -->
            <div class="text-center">
              <p class="text-sm text-gray-600">
                Already have an account?
                <a
                  href="#"
                  class="text-blue-500 hover:text-blue-600 font-medium"
                >
                  Sign in
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
const phone = ref("");
const password = ref("");
const confirmPassword = ref("");
const showPassword = ref(false);
const acceptTerms = ref(false);

const handleSignup = () => {
  if (
    !email.value ||
    !phone.value ||
    !password.value ||
    !confirmPassword.value
  ) {
    console.log("Please fill all fields");
    return;
  }

  if (password.value !== confirmPassword.value) {
    console.log("Passwords do not match");
    return;
  }

  if (!acceptTerms.value) {
    console.log("Please accept terms and conditions");
    return;
  }

  console.log("Signup:", {
    email: email.value,
    phone: phone.value,
    password: password.value,
  });
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
