<script lang="ts">
    import logo from "$lib/assets/logo.webp"
  import { onMount } from 'svelte';
  let isMenuOpen = false;
  let isScrolled = false;

  function toggleMenu() {
    isMenuOpen = !isMenuOpen;
  }

  onMount(() => {
    const handleScroll = () => {
      isScrolled = window.scrollY > 0;
    };
    window.addEventListener('scroll', handleScroll);
    return () => {
      window.removeEventListener('scroll', handleScroll);
    };
  });
</script>

<header class="sticky w-full h-fit z-50 transition-all duration-300 {isScrolled ? 'bg-white shadow-md' : 'bg-transparent'}">

  <!-- Main Navigation -->
  <nav class="bg-white md:bg-transparent py-4 px-4">
    <div class="container mx-auto flex justify-between items-center">
      <!-- Logo -->
      <a href="/" class="flex items-center space-x-2">
        <img src={logo} alt="Ortiz Logo" class="h-[5rem]" /> 
      </a>

      <!-- Desktop Menu -->
      <ul class="hidden lg:flex space-x-8 text-lg font-medium text-gray-700">
        <li><a href="/" class="hover:text-[#30A7E3]">Home</a></li>
        <li><a href="/services" class="hover:text-[#30A7E3]">Services</a></li>
        <li><a href="/features" class="hover:text-[#30A7E3]">Features</a></li>
        <li><a href="/properties" class="hover:text-[#30A7E3]">Properties</a></li>
        <li><a href="/pages" class="hover:text-[#30A7E3]">Pages</a></li>
        <li><a href="/agent" class="hover:text-[#30A7E3]">Agent</a></li>
        <li><a href="/contact" class="hover:text-[#30A7E3]">Contact</a></li>
      </ul>

      <!-- Search Icon (Desktop) -->
      <div class="hidden lg:block">
        <button class="text-gray-700 hover:text-[#30A7E3]">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" />
          </svg>
        </button>
      </div>

      <!-- Mobile Menu Button -->
      <div class="lg:hidden">
        <button on:click={toggleMenu} class="text-gray-700 focus:outline-none focus:text-[#30A7E3]">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
          </svg>
        </button>
      </div>
    </div>
  </nav>

  <!-- Mobile Menu / Sidebar -->
  <div
    class="fixed top-0 right-0 w-64 bg-white h-full shadow-lg transform {isMenuOpen ? 'translate-x-0' : 'translate-x-full'}
    transition-transform duration-300 ease-in-out lg:hidden"
  >
    <div class="p-4">
      <button on:click={toggleMenu} class="text-gray-700 focus:outline-none float-right">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
        </svg>
      </button>
      <ul class="mt-8 space-y-4 text-lg font-medium text-gray-700">
        <li><a href="/" class="block hover:text-[#30A7E3]" on:click={toggleMenu}>Home</a></li>
        <li><a href="/services" class="block hover:text-[#30A7E3]" on:click={toggleMenu}>Services</a></li>
        <li><a href="/features" class="block hover:text-[#30A7E3]" on:click={toggleMenu}>Features</a></li>
        <li><a href="/properties" class="block hover:text-[#30A7E3]" on:click={toggleMenu}>Properties</a></li>
        <li><a href="/pages" class="block hover:text-[#30A7E3]" on:click={toggleMenu}>Pages</a></li>
        <li><a href="/agent" class="block hover:text-[#30A7E3]" on:click={toggleMenu}>Agent</a></li>
        <li><a href="/contact" class="block hover:text-[#30A7E3]" on:click={toggleMenu}>Contact</a></li>
      </ul>
    </div>
  </div>
</header>

<style lang="postcss">
  :global(html) {
    scroll-padding-top: 5rem; /* Adjust this value based on your header height */
  }
</style>