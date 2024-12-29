<script lang="ts">
  import ServiceHeader from '$lib/components/ServiceHeader.svelte';
</script>

<svelte:head>
  <title>Business Process Management - Holon Management Consulting</title>
</svelte:head>

<div class="bg-white py-24 sm:py-32">
  <div class="mx-auto max-w-7xl px-6 lg:px-8">
    <ServiceHeader
      title="Business Process Management"
      description="Optimize and streamline your business processes for maximum efficiency and effectiveness."
    />
    
    <div class="mx-auto mt-16 max-w-2xl lg:max-w-none">
      <div class="grid grid-cols-1 gap-8 lg:grid-cols-2">
        <div class="bg-gray-50 p-8 rounded-lg">
          <h3 class="text-xl font-semibold mb-4">Process Optimization</h3>
          <p class="text-gray-600">Streamline and improve business processes to enhance operational efficiency and reduce costs.</p>
        </div>
        <div class="bg-gray-50 p-8 rounded-lg">
          <h3 class="text-xl font-semibold mb-4">Workflow Automation</h3>
          <p class="text-gray-600">Implement automated solutions to streamline repetitive tasks and improve productivity.</p>
        </div>
      </div>
    </div>
  </div>
</div>