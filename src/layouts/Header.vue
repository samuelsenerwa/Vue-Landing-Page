<script setup>
import { ref } from "vue";

let mobileNav = ref(false);
let toggleMobileNav = () => {
  mobileNav.value = !mobileNav.value;
};
</script>

<template>
  <!-- Navbar starts -->
  <div class="container mx-auto px5">
    <header class="flex justify-between py-12 items-center">
      <div>
        <a href="/"><img src="/images/logo-bookmark.svg" alt="Site Logo" /></a>
      </div>
      <nav class="flex justify-end flex-col md:flex-row">
        <!-- Menu Toggler -->
        <button type="button" class="flex md:hidden focus:outline-none">
          <svg viewBox="0 0 24 24" class="h-6 w-6 fill-current">
            <path
              fill-rule="evenodd"
              d="M4 5h16a1 1 0 0 1 0 2H4a1 1 0 1 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2z"
            ></path>
          </svg>
        </button>

        <!-- Desktop Menu -->
        <ul
          class="space-x-10 font-theme-heading font-medium items-center hidden md:flex flex-col space-y-7 md:space-y-0 md:flex-row"
        >
          <li
            class="uppercase hover:text-theme-secondary transition duration-200"
          >
            <a href="#features" v-smooth-scroll>Features</a>
          </li>
          <li
            class="uppercase hover:text-theme-secondary transition duration-200"
          >
            <a href="#features" v-smooth-scroll>FAQ</a>
          </li>
          <li
            class="uppercase hover:text-theme-secondary transition duration-200"
          >
            <a href="#subscribe" v-smooth-scroll>Subscribe</a>
          </li>
          <li
            class="uppercase bg-theme-secondary px-6 py-2 text-white rounded shadow-md hover:bg-white border-2 border-transparent hover:border-theme-secondary hover:text-theme-secondary cursor-pointer transition duration-200"
          >
            <a href="#download-section" v-smooth-scroll>Download</a>
          </li>
        </ul>
      </nav>
    </header>

    <!-- Mobile Menu Start -->

    <div v-show="mobileNav">
      <div
        class="absolute px-5 py-12 block z-30 top-0 left-0 w-full h-full bg-gradient-to-b from-theme-dark-blue via-theme-dark-blue-tp to-theme-dark-blue"
      >
        <div></div>
      </div>
    </div>

    <!-- Mobile Menu End -->
  </div>
</template>