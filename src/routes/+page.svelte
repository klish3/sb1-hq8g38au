<script lang="ts">
  import ValueProposition from '$lib/components/ValueProposition.svelte';

  const services = [
    {
      title: 'Strategy Consulting',
      description: 'Develop and implement effective business strategies for sustainable growth.',
      href: '/strategy-consulting'
    },
    {
      title: 'Business Analysis',
      description: 'Transform data into actionable insights for better decision-making.',
      href: '/business-analysis'
    },
    {
      title: 'Business Process Management',
      description: 'Optimize and streamline your business processes for maximum efficiency.',
      href: '/business-process-management'
    },
    {
      title: 'Executive Coaching',
      description: 'Empower your leadership team with personalized coaching services.',
      href: '/executive-coaching'
    }
  ];
</script>

<svelte:head>
  <title>Holon Management Consulting - Strategy & Business Intelligence</title>
</svelte:head>

<div class="bg-white">
  <!-- Hero Section -->
  <div class="relative bg-gray-900">
    <div class="max-w-7xl mx-auto py-24 px-4 sm:py-32 sm:px-6 lg:px-8">
      <h1 class="text-4xl font-extrabold tracking-tight text-white sm:text-5xl lg:text-6xl">
        Transform Your Business with Strategic Insights
      </h1>
      <p class="mt-6 text-xl text-gray-300 max-w-3xl">
        Holon Management Consulting helps organizations increase profitability through improved effectiveness and efficiency.
      </p>
      <div class="mt-10">
        <a href="/contact" class="inline-flex items-center px-6 py-3 border border-transparent text-base font-medium rounded-md text-white bg-blue-600 hover:bg-blue-700">
          Get Started
        </a>
      </div>
    </div>
  </div>

  <!-- Value Proposition Section -->
  <ValueProposition />

  <!-- Services Section -->
  <div class="py-12 bg-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="lg:text-center">
        <h2 class="text-3xl font-extrabold text-gray-900 sm:text-4xl">Our Services</h2>
        <p class="mt-4 max-w-2xl text-xl text-gray-500 lg:mx-auto">
          Comprehensive consulting solutions tailored to your business needs.
        </p>
      </div>

      <div class="mt-10">
        <div class="grid grid-cols-1 gap-10 sm:grid-cols-2">
          {#each services as {title, description, href}}
            <a {href} class="p-6 bg-gray-50 rounded-lg transition-transform hover:scale-105">
              <h3 class="text-lg font-medium text-gray-900">{title}</h3>
              <p class="mt-2 text-gray-500">{description}</p>
            </a>
          {/each}
        </div>
      </div>
    </div>
  </div>
</div>