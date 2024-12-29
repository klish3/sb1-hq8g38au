<script lang="ts">
  const metrics = [
    { value: '31%', description: 'reduction in operational costs for a mid-size bank' },
    { value: '66%', description: 'unit cost reduction by eliminating waste' },
    { value: '50%', description: 'increase in processing capacity through creation of a shared services environment' },
    { value: '40%', description: 'reduction in Turn-Around-time' }
  ];
</script>

<section class="py-16 bg-gray-50">
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
    <h2 class="text-3xl font-bold text-gray-900 text-center mb-12">Value Delivered</h2>
    
    <div class="grid grid-cols-1 gap-8 md:grid-cols-2 lg:grid-cols-4">
      {#each metrics as {value, description}}
        <div class="bg-white p-6 rounded-lg shadow-sm text-center">
          <p class="text-4xl font-bold text-blue-600 mb-2">{value}</p>
          <p class="text-gray-600">{description}</p>
        </div>
      {/each}
    </div>
  </div>
</section>