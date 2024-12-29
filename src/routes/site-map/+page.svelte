<script lang="ts">
  const siteStructure = [
    {
      title: 'Main Pages',
      links: [
        { href: '/', label: 'Home' },
        { href: '/about', label: 'About' },
        { href: '/contact', label: 'Contact' }
      ]
    },
    {
      title: 'Services',
      links: [
        { href: '/services', label: 'Services Overview' },
        { href: '/services/strategy-consulting', label: 'Strategy Consulting' },
        { href: '/services/business-analysis', label: 'Business Analysis' },
        { href: '/services/business-process-management', label: 'Business Process Management' },
        { href: '/services/executive-coaching', label: 'Executive Coaching' }
      ]
    }
  ];
</script>

<svelte:head>
  <title>Site Map - Holon Management Consulting</title>
</svelte:head>

<div class="bg-white py-24 sm:py-32">
  <div class="mx-auto max-w-7xl px-6 lg:px-8">
    <h1 class="text-4xl font-bold text-gray-900 mb-12">Site Map</h1>
    
    <div class="grid grid-cols-1 gap-12 lg:grid-cols-2">
      {#each siteStructure as section}
        <div>
          <h2 class="text-2xl font-semibold text-gray-900 mb-6">{section.title}</h2>
          <ul class="space-y-4">
            {#each section.links as {href, label}}
              <li>
                <a
                  {href}
                  class="text-blue-600 hover:text-blue-800 transition-colors"
                >
                  {label}
                </a>
              </li>
            {/each}
          </ul>
        </div>
      {/each}
    </div>
  </div>
</div>