<script lang="ts">
  import '../app.css';
  import Navigation from '../lib/components/Navigation.svelte';
  import Footer from '../lib/components/Footer.svelte';
</script>

<div class="min-h-screen bg-white">
  <Navigation />
  <main>
    <slot />
  </main>
  <Footer />
</div>