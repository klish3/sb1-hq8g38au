<script lang="ts">
  import Navigation from './lib/components/Navigation.svelte';
  import Footer from './lib/components/Footer.svelte';
  import Home from './routes/+page.svelte';
</script>

<div class="min-h-screen bg-white">
  <Navigation />
  <main>
    <Home />
  </main>
  <Footer />
</div>