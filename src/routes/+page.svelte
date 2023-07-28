<script>
  import Navbar from "$lib/Navbar.svelte";
</script>

<div id="app-container">
  <Navbar />
  <h1>Welcome to SvelteKit</h1>
  <p>
    Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation
  </p>
</div>

<style>
  #app-container {
    width: min(80%, 1440px);
    margin: 0 auto;
  }
</style>
