<script setup>
import Onboarding from "./components/onBoarding.vue";
import Login from "./components/Login.vue";
import SignUp from "./components/signUp.vue";
import DeliveryDetails from "./components/deliverydetails.vue";
import { ref } from "vue";
import Loadingpage from "./components/loadingpage.vue";
import OrderSuccess from "./components/ordersuccess.vue";
</script>

<template>
  <div class="w-full min-h-screen bg-white">
    <Onboarding />
    <Login />
    <SignUp />
    <DeliveryDetails />
    <Loadingpage />
    <OrderSuccess />
  </div>
</template>

<style scoped></style>
