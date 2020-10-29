<template>
  <div>
    <div class="home flex justify-center p-1  ">
      <Navbar />
    </div>
    <!-- <img alt="Vue logo" src="../assets/logo.png" /> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App" /> -->
    <!-- <h2 class="text-4xl">Welcome To My Site</h2> -->
    <InputForm/>
  </div>
</template>

<script>
import Navbar from "@/components/Navbar.vue";
import InputForm from "@/components/InputForm.vue";
export default {
  name: "Home",
  components: {
    Navbar,
    InputForm
  }
};
</script>


