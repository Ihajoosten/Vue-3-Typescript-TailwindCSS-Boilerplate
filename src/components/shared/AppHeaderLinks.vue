<template>
  <!-- Header links -->
  <div
    :class="isOpen ? 'block' : 'hidden'"
    class="m-0 sm:ml-4 mt-5 sm:mt-3 sm:flex p-5 sm:p-0 justify-center items-center shadow-lg sm:shadow-none"
  >
    <router-link
      to="/"
      class="font-general-medium block text-left text-lg font-medium text-primary-dark dark:text-ternary-light hover:text-indigo-600 dark:hover:text-indigo-300 sm:mx-4 mb-2 sm:py-2"
      aria-label="Projects"
      >Home</router-link
    >
    <router-link
      to="/login"
      class="font-general-medium block text-left text-lg font-medium text-primary-dark dark:text-ternary-light hover:text-indigo-600 dark:hover:text-indigo-300 sm:mx-4 mb-2 sm:py-2 border-t-2 pt-3 sm:pt-2 sm:border-t-0 border-primary-light dark:border-secondary-dark"
      aria-label="About Me"
      >Login</router-link
    >
    <router-link
      to="/register"
      class="font-general-medium block text-left text-lg font-medium text-primary-dark dark:text-ternary-light hover:text-indigo-600 dark:hover:text-indigo-300 sm:mx-4 mb-2 sm:py-2 border-t-2 pt-3 sm:pt-2 sm:border-t-0 border-primary-light dark:border-secondary-dark"
      aria-label="Contact"
      >Sign up</router-link
    >
    <div
      class="border-t-2 pt-3 sm:pt-0 sm:border-t-0 border-primary-light dark:border-secondary-dark"
    >
      <Button
        title="Click me"
        class="font-general-medium sm:hidden block text-left text-md font-medium bg-indigo-500 hover:bg-indigo-600 text-white shadow-sm rounded-sm px-4 py-2 mt-2 duration-500"
        aria-label="Click me"
      />
    </div>
  </div>
</template>

<script lang="ts">
import Button from "@/components/reusable/ButtonComponent.vue";

export default {
  components: {
    Button,
  },
  props: ["isOpen"],
};
</script>
