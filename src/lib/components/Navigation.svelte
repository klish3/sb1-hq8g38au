<script lang="ts">
  import { page } from '$app/stores';

  const navItems = [
    { href: '/strategy-consulting', label: 'Strategy Consulting' },
    { href: '/business-analysis', label: 'Business Analysis' },
    { href: '/business-process-management', label: 'Business Process Management' },
    { href: '/executive-coaching', label: 'Executive Coaching' }
  ];

  let isMenuOpen = false;
  const toggleMenu = () => isMenuOpen = !isMenuOpen;
</script>

<nav class="bg-white shadow-lg">
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
    <div class="flex justify-between h-16">
      <div class="flex">
        <div class="flex-shrink-0 flex items-center">
          <a href="/" class="text-2xl font-bold text-gray-800">Holon</a>
        </div>
      </div>

      <!-- Desktop Navigation -->
      <div class="hidden md:flex md:items-center md:space-x-4">
        {#each navItems as {href, label}}
          <a
            {href}
            class="text-gray-900 px-3 py-2 rounded-md text-sm font-medium hover:bg-gray-100 transition-colors"
            class:bg-gray-100={$page.url.pathname === href}
            data-sveltekit-preload
          >
            {label}
          </a>
        {/each}
      </div>

      <!-- Mobile menu button -->
      <div class="flex items-center md:hidden">
        <button
          on:click={toggleMenu}
          class="inline-flex items-center justify-center p-2 rounded-md text-gray-700 hover:bg-gray-100 focus:outline-none"
          aria-expanded="false"
        >
          <span class="sr-only">Open main menu</span>
          <svg
            class="h-6 w-6"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
          >
            {#if isMenuOpen}
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
            {:else}
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
            {/if}
          </svg>
        </button>
      </div>
    </div>
  </div>

  <!-- Mobile Navigation -->
  {#if isMenuOpen}
    <div class="md:hidden">
      <div class="px-2 pt-2 pb-3 space-y-1">
        {#each navItems as {href, label}}
          <a
            {href}
            class="block px-3 py-2 rounded-md text-base font-medium text-gray-900 hover:bg-gray-100 transition-colors"
            class:bg-gray-100={$page.url.pathname === href}
            data-sveltekit-preload
          >
            {label}
          </a>
        {/each}
      </div>
    </div>
  {/if}
</nav>