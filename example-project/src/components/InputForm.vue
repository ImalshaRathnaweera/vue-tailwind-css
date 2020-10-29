<template>
  <div>
    <div class="flex justify-center pt-10">
      <div class="w-full max-w-2xl">
        <form
          class="bg-white shadow-md rounded-xl px-8 pt-6 pb-8 mb-4 w-full"
          @submit="register"
        >
          <h4 class="flex justify-center text-3xl font-semibold">
            Registration
          </h4>
          <div class="flex justify-center">
            <img alt="" src="../assets/registration.png" class="w-56 h-56" />
          </div>
          <label
            class="block text-gray-900 text-sm font-semibold mb-2"
            for="firstname"
          >
            First Name
          </label>
          <input
            type="text"
            class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
            placeholder="Enter First Name"
            v-model="firstname"
          />

          <label
            class="block text-gray-900 text-sm font-semibold mb-2"
            for="lastname"
          >
            Last Name
          </label>
          <input
            type="text"
            class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
            placeholder="Enter Last Name "
            v-model="lastname"
          />

          <label
            class="block text-gray-900 text-sm font-semibold mb-2"
            for="email"
          >
            Email
          </label>
          <input
            type="text"
            class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
            placeholder="Enter Email Address"
            v-model="email"
          />

          <label
            class="block text-gray-900 text-sm font-semibold mb-2"
            for="password"
          >
            Password
          </label>
          <input
            type="password"
            class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
            placeholder="Enter Password"
            v-model="password"
          />
          <div class="flex justify-center pt-4">
            <button type ="submit"
              class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded"
            >
              Submit
            </button>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "InputForm",
  data() {
    return {
      error: [],
      firstname: null,
      lastname: null,
      email: null,
      password: null
    };
  },
  methods: {
    register(e) {
      if (this.firstname && this.lastname && this.email && this.password) {
        console.log("Registration Succuessful");

      }
      this.error = [];
      if (!this.firstname) {
        this.error.push("First name is required");
      }
      if (!this.lastname) {
        this.error.push("Last name is required");
      }
      if (!this.email) {
        this.error.push("Email is required");
      }
      if (!this.password) {
        this.error.push("Password is required");
      }
      console.warn("error",this.error)
      e.preventDefault();
    }
  }
};
</script>

<style>
</style>