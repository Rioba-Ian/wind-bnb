<script>
  import Navbar from "$lib/Navbar.svelte";
  import Stay from "$lib/Stay.svelte";
</script>

<div id="app-container">
  <Navbar />
  <main class="py-8">
    <div id="title" class="flex items-center justify-between">
      <h1 class="text-neutral-800 text-3xl font-bold">Stays in Finland</h1>
      <p>+stays</p>
    </div>
    <div id="content" class="py-5">
      <Stay />
    </div>
  </main>
</div>

<style>
  #app-container {
    width: min(80%, 1440px);
    margin: 0 auto;
  }
</style>
