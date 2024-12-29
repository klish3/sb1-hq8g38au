<script lang="ts">
  import { expertiseItems } from '$lib/data/services';
</script>

<svelte:head>
  <title>Services - Holon Management Consulting</title>
</svelte:head>

<div class="bg-white py-24 sm:py-32">
  <div class="mx-auto max-w-7xl px-6 lg:px-8">
    <div class="mx-auto max-w-2xl lg:text-center">
      <h2 class="text-base font-semibold leading-7 text-blue-600">Our Expertise</h2>
      <p class="mt-2 text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl">
        Comprehensive Consulting Services
      </p>
      <p class="mt-6 text-lg leading-8 text-gray-600">
        We offer a wide range of consulting services to help organizations optimize their operations and achieve sustainable growth.
      </p>
    </div>
    
    <div class="mx-auto mt-16 max-w-2xl sm:mt-20 lg:mt-24 lg:max-w-none">
      <dl class="grid max-w-xl grid-cols-1 gap-x-8 gap-y-16 lg:max-w-none lg:grid-cols-3">
        {#each expertiseItems as {title, description}}
          <div class="flex flex-col">
            <dt class="font-semibold text-gray-900">{title}</dt>
            <dd class="mt-4 flex flex-auto flex-col text-base leading-7 text-gray-600">
              <p>{description}</p>
            </dd>
          </div>
        {/each}
      </dl>
    </div>
  </div>
</div>