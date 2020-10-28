<template>
  <div>
    <div class="home flex justify-center p-1  ">
      <Navbar/>
    </div>
    <!-- <img alt="Vue logo" src="../assets/logo.png" /> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App" /> -->
    <!-- <h2 class="text-4xl">Welcome To My Site</h2> -->
    <div class="flex justify-center pt-10">
      <div class="w-full max-w-2xl">
        <form class="bg-white shadow-md rounded-xl px-8 pt-6 pb-8 mb-4 w-full">
          <h4 class="flex justify-center text-3xl font-semibold">
            Registration
          </h4>
          <div class="flex justify-center">
            <img alt="" src="../assets/registration.png" class="w-56 h-56" />
          </div>
          <label
            class="block text-gray-900 text-sm font-semibold mb-2"
            for="username"
          >
            First Name
          </label>
          <InputForm placeholder="enter name" />

          <label
            class="block text-gray-900 text-sm font-semibold mb-2"
            for="username"
          >
            Last Name
          </label>
          <InputForm />

          <label
            class="block text-gray-900 text-sm font-semibold mb-2"
            for="username"
          >
            Email
          </label>
          <InputForm />

          <label
            class="block text-gray-900 text-sm font-semibold mb-2"
            for="username"
          >
            Address
          </label>
          <InputForm />
        </form>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";
import Navbar from "@/components/Navbar.vue";
import InputForm from "@/components/InputForm.vue";
export default {
  name: "Home",
  components: {
    // HelloWorld
    Navbar,
    InputForm
  }
};
</script>

<style>
</style>
